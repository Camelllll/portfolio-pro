<script setup>
import { onMounted } from 'vue';
import AboutView from '@/views/AboutView.vue';
import ProjectView from '@/views/ProjectView.vue';
import ContactView from '@/views/ContactView.vue';

onMounted(() => {
  const links = document.querySelectorAll('.navbar a, .navbar button');

  links.forEach(link => {
    link.addEventListener('click', (event) => {
      event.preventDefault();
      const targetId = link.getAttribute('href') ? link.getAttribute('href').substring(1) : null;

      if (link.textContent.trim() === 'Contact') {
        const contactElement = document.getElementById('contact');
        if (contactElement) {
          window.scrollTo({
            top: contactElement.offsetTop + window.innerHeight * 2,
            behavior: 'smooth'
          });
        }
      } else if (targetId) {
        const targetElement = document.getElementById(targetId);
        if (targetElement) {
          window.scrollTo({
            top: targetElement.offsetTop,
            behavior: 'smooth'
          });
        }
      }
    });
  });
});
</script>

<template>
  <div>
    <section id="home" class="section home">
      <div class="content">
        <header>
          <div class="wrapper">
            <nav class="navbar">
              <a href="#home" class="title-link">
                <h1 class="logo_title"> Camélien</h1>
                <h2 class="subtitle_title">Développeur Web</h2>
              </a>

              <div class="nav-links">
                <a href="#about">À Propos</a>
                <a href="#projects">Projets</a>
                <button class="btn">
                  Contact
                </button>
              </div>
            </nav>
          </div>
        </header>
        <main class="centered">
          <h1>Développeur Web Full Stack</h1>
          <h2>Passionné par le 
            <span class="letter color-span">d</span>
            <span class="letter color-span">é</span>
            <span class="letter color-span">v</span>
            <span class="letter color-span">e</span>
            <span class="letter color-span">l</span>
            <span class="letter color-span">o</span>
            <span class="letter color-span">p</span>
            <span class="letter color-span">p</span>
            <span class="letter color-span">e</span>
            <span class="letter color-span">m</span>
            <span class="letter color-span">e</span>
            <span class="letter color-span">n</span>
            <span class="letter color-span">t</span>
            <span class="letter">&nbsp;</span>
            <span class="letter color-span">w</span>
            <span class="letter color-span">e</span>
            <span class="letter color-span">b</span>
            et les nouvelles technologies</h2>
          <div class="center-img">
            <img src="@/assets/img/mf-avatar.svg" alt="developer" />
          </div>
        </main>
      </div>
    </section>

    <section id="about" class="section">
      <AboutView />
    </section>

    <section id="projects" class="section">
      <ProjectView />
    </section>

    <section id="contact" class="section">
      <ContactView />
    </section>

  </div>
</template>

<style scoped lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Rubik:ital,wght@0,300..900;1,300..900&display=swap');
@import url('https://fonts.googleapis.com/css2?family=REM:ital,wght@0,100..900;1,100..900&display=swap');
@import url('https://fonts.cdnfonts.com/css/gilroy-bold');

// animation delay
.letter:nth-child(1) { animation-delay: 0.1s; }
.letter:nth-child(2) { animation-delay: 0.2s; }
.letter:nth-child(3) { animation-delay: 0.3s; }
.letter:nth-child(4) { animation-delay: 0.4s; }
.letter:nth-child(5) { animation-delay: 0.5s; }
.letter:nth-child(6) { animation-delay: 0.6s; }
.letter:nth-child(7) { animation-delay: 0.7s; }
.letter:nth-child(8) { animation-delay: 0.8s; }
.letter:nth-child(9) { animation-delay: 0.9s; }
.letter:nth-child(10) { animation-delay: 1s; }
.letter:nth-child(11) { animation-delay: 1.1s; }
.letter:nth-child(12) { animation-delay: 1.2s; }
.letter:nth-child(13) { animation-delay: 1.3s; }
.letter:nth-child(14) { animation-delay: 1.4s; }
.letter:nth-child(15) { animation-delay: 1.5s; }
.letter:nth-child(16) { animation-delay: 1.6s; }
.letter:nth-child(17) { animation-delay: 1.7s; }

.letter {
  display: inline-block;
  opacity: 0;
  transform: translateY(20px);
  animation: jumpIn 0.8s forwards;
}

// Key Frames
@keyframes jumpIn {
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

* {
  font-family: 'Gilroy-Bold', sans-serif;
  font-weight: 400;
}

.background {
  position: relative;
  height: 100vh;
}

.color-span {
  color: #7510f6;
}

.section {
  height: 100vh;
  position: relative;
  background-color: #fff;
}

.content {
  position: relative;
  z-index: 1;
}

.btn {
  padding: 10px 20px;
  background-color: transparent;
  border: 2px solid #7510f6;
  color: #7510f6;
  border-radius: 5px;
  cursor: pointer;
  transition: all 0.3s ease;
  font-family: 'Gilroy-Bold', sans-serif;
  font-weight: 400;
  font-size: 14px;

  &:hover {
    background-color: #7510f6;
    color: white;
  }
}

.wrapper {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 20px;
}

.title-link {
  display: flex;
  flex-direction: column;
  color: #141c3a;
  text-decoration: none;

  .logo_title {
    font-size: 30px;
    font-weight: 700;
    line-height: 1.2;
    font-family: 'Gilroy-Bold', sans-serif;
    font-weight: 400;
  }

  .subtitle_title {
    font-size: 12px;
    font-weight: 600;
    line-height: 0.3;
    font-family: 'Gilroy-Bold', sans-serif;
    font-weight: 400;
    margin-left: 14px;
    color: #7510f6;
  }
}

.centered {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 89vh;
  text-align: center;
  color: #141c3a;
  font-family: 'Gilroy-Medium', sans-serif;
  padding: 0 20px;

  h1 {
    font-size: 44px;
    font-weight: 700;
  }

  h2 {
    font-size: 24px;
    font-weight: 400;
  }
}

.center-img {
  margin-top: 20px;
  img {
    width: 230px;
    height: 230px;
    border-radius: 50%;
  }
}

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
}

.nav-links {
  display: flex;
  align-items: center;
  gap: 30px;
  margin-top: 10px;
}

.nav-links a, .nav-links button {
  text-decoration: none;
  color: #141c3a;
  font-size: 16px;
  font-family: 'Gilroy-Bold', sans-serif;
  font-weight: 500;
  transition: all 0.3s ease;

  &:hover {
    color: #7510f6;
  }
}

#about {
  background-color: #7510f6;
  text-align: center;
}

@media screen and (max-width: 768px) {
  .wrapper {
    flex-direction: column;
    gap: 10px;
  }

  .title-link {
    margin: 0;
    align-items: center;

    .logo_title {
      font-size: 24px;
    }

    .subtitle_title {
      font-size: 10px;
      margin-left: 0;
    }
  }

  .navbar {
    flex-direction: column;
    gap: 10px;
  }

  .nav-links {
    flex-direction: column;
    gap: 15px;
  }

  .centered h1 {
    font-size: 36px;
  }

  .centered h2 {
    font-size: 18px;
  }

  .center-img img {
    width: 180px;
    height: 180px;
  }
}

@media screen and (max-width: 480px) {
  .navbar {
    gap: 10px;
  }

  .centered h1 {
    font-size: 28px;
  }

  .centered h2 {
    font-size: 16px;
  }

  .center-img img {
    width: 150px;
    height: 150px;
  }
}
</style>