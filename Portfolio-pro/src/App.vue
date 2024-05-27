<script setup>
import { RouterLink, RouterView } from 'vue-router'
import AboutView from '@/views/AboutView.vue';
</script>

<template>
  <div>
    <section class="section home">
      <div class="content">
        <header>
          <div class="wrapper">
            <nav class="navbar">
              <RouterLink to="/" class="title-link">
                <h1 class="logo_title"> Camélien</h1>
                <h2 class="subtitle_title">Développeur Web</h2>
              </RouterLink>

              <RouterLink to="/about">À Propos</RouterLink>
              <RouterLink to="/projects">Projets</RouterLink>
                <RouterLink to="/contact">
                  <button class="btn">
                    Contact
                  </button>
                </RouterLink>
            </nav>
          </div>
        </header>
        <main class="centered">
          <h1>Développeur Web Full Stack</h1>
          <h2>Passionné par le<span class="color-span">développement web</span>  et les nouvelles technologies</h2>
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

  </div>
</template>

<style scoped lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Rubik:ital,wght@0,300..900;1,300..900&display=swap');
@import url('https://fonts.googleapis.com/css2?family=REM:ital,wght@0,100..900;1,100..900&display=swap');
@import url('https://fonts.cdnfonts.com/css/gilroy-bold');


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
}

.title-link {
  display: flex;
  flex-direction: column;
  color: #141c3a;
  text-decoration: none;
  margin-right: 790px;
  margin-left: 80px;

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
  align-items: center;
  gap: 30px;
  margin-top: 20px;
  

  a {
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
}

#about {
  background-color: #7510f6;
  text-align: center;
}
</style>