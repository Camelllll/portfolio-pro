<template>
  <div class="myproject">
    <div class="projects">
      <h1>Mes récents projets</h1>
      <p>Voici quelques projets sur lesquels j'ai travaillé récemment.</p>
      <p>Vous voulez en savoir plus ? <a href="mailto:camelien.tournu@gmail.com">Contactez-moi</a></p>
    </div>

    <div class="project-grid">
      <div class="project-card card-1">
        <div class="project-card-inner">
          <div class="project-card-front">
            <div class="overlay"></div>
            <div class="project-info">
              <h3>Pokedex React Native</h3>
            </div>
          </div>
          <div class="project-card-back">
            <div class="back-info">
              <p>Création d'une application Pokedex avec React Native.</p>
              <a href="https://github.com/Camelllll/PokedexReact.git" target="_blank">
                <button>Voir le projet</button>
              </a>
            </div>
          </div>
        </div>
      </div>

      <div class="project-card card-2">
        <div class="project-card-inner">
          <div class="project-card-front">
            <div class="overlay"></div>
            <div class="project-info">
              <h3>I Hate PDF</h3>
            </div>
          </div>
          <div class="project-card-back">
            <div class="back-info">
              <p>Création d'un site web pour génération de pdf en microservice.</p>
              <a href="https://github.com/Camelllll/WR602D-WEBAPP.git" target="_blank">
                <button>Voir le projet</button>
              </a>
            </div>
          </div>
        </div>
      </div>

      <div class="project-card card-3">
        <div class="project-card-inner">
          <div class="project-card-front">
            <div class="overlay"></div>
            <div class="project-info">
              <h3>TMA</h3>
            </div>
          </div>
          <div class="project-card-back">
            <div class="back-info">
              <p>Création de mon premier site web en 2022 pour l'entreprise TMA.</p>
              <a href="https://we.tl/t-O170MmxCmV">
                <button>Voir le projet</button>
              </a>
            </div>
          </div>
        </div>
      </div>

      <div class="project-card card-4">
        <div class="project-card-inner">
          <div class="project-card-front">
            <div class="overlay"></div>
            <div class="project-info">
              <h3>Ammaé</h3>
            </div>
          </div>
          <div class="project-card-back">
            <div class="back-info">
              <p>Création d'un site vitrine dynamique et attrayant 
                pour une entreprise de service de massages à domicile.</p>
              <a href="https://www.ammae.fr" target="_blank">
                <button>Voir le projet</button>
              </a>
            </div>
          </div>
        </div>
      </div>

      <div class="project-card card-5">
        <div class="project-card-inner">
          <div class="project-card-front">
            <div class="overlay"></div>
            <div class="project-info">
              <h3>Soon...</h3>
            </div>
          </div>
          <div class="project-card-back">
            <div class="back-info">
              <p>ce projet est en cours de réalisation, il sera disponible très bientôt !</p>
            </div>
          </div>
        </div>
      </div>

      <div class="project-card card-6">
        <div class="project-card-inner">
          <div class="project-card-front">
            <div class="overlay"></div>
            <div class="project-info">
              <h3>Soon...</h3>
            </div>
          </div>
          <div class="project-card-back">
            <div class="back-info">
              <p>ce projet est en cours de réalisation, il sera disponible très bientôt !</p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="contact-button-container">
      <a href="https://github.com/Camelllll" target="_blank">
        <button class="btn">En voir plus sur GitHub</button>
      </a>
    </div>
  </div>
</template>

<style scoped>
.myproject {
  background-color: #fff;
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  z-index: 1;

  h1 {
    font-size: 36px;
    color: #000;
    z-index: 2;
    margin-top: 65vh;
  }

  p {
    font-size: 18px;
    color: #000;
    z-index: 2;
  }
}

.projects {
  position: absolute;
  z-index: 2;
  text-align: center;

  a {
    color: #7510f6;
    text-decoration: none;
  }

  a:hover {
    text-decoration: underline;
  }
}

.project-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 50px;
  margin-top: 190vh;
  z-index: 2;
  text-align: center;
  padding: 0 20px;
}

.project-card {
  width: 370px;
  height: 270px;
  perspective: 1000px;
  border-radius: 10px;
}

.project-card-inner {
  width: 100%;
  height: 100%;
  text-align: center;
  transition: transform 0.6s;
  transform-style: preserve-3d;
  position: relative;
}

.project-card:hover .project-card-inner {
  transform: rotateY(180deg);
}

.project-card-front, .project-card-back {
  position: absolute;
  width: 100%;
  height: 100%;
  backface-visibility: hidden;
  border-radius: 10px;
}

.project-card-front {
  background-size: cover;
  background-position: center;
}

.card-1 .project-card-front {
  background-image: url('@/assets/img/ronflex.png');
}

.card-2 .project-card-front {
  background-image: url('@/assets/img/pdf.jpg');
}

.card-3 .project-card-front {
  background-image: url('@/assets/img/administratif.jpeg');
}

.card-4 .project-card-front {
  background-image: url('@/assets/img/massage.jpg');
}

.card-5 .project-card-front {
  background-image: url('@/assets/img/projetsoon.jpeg');
}

.card-6 .project-card-front {
  background-image: url('@/assets/img/projetsoon2.jpg');
}

.project-card-back {
  background-color: #333;
  color: white;
  transform: rotateY(180deg);
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  z-index: 1;
}

.overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  border-radius: 10px;
  z-index: 1;
}

.project-info {
  position: relative;
  z-index: 2;
  color: white;
  text-align: center;
  margin-top: 110px;

  h3 {
    font-size: 22px;
    font-weight: 600;
  }
}

.back-info {
  text-align: center;

  p {
    font-size: 18px;
    margin-bottom: 20px;
    color: white;
    padding: 30px;
  }
  
  button {
    padding: 10px 20px;
    background-color: transparent;
    border: 2px solid #7510f6;
    color: #ffffff;
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
}

.contact-button-container {
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 2;
  margin-top: 50px;

  a {
    color: white;
    text-decoration: none;
  }
}

.btn {
  padding: 15px 30px;
  background-color: #7510f6;
  border: 2px solid #7510f6;
  color: white;
  border-radius: 25px;
  cursor: pointer;
  transition: all 0.3s ease;
  font-family: 'Gilroy-Bold', sans-serif;
  font-weight: 400;
  font-size: 18px;

  &:hover {
    background-color: #37007f;
    color: white;
  }
}

@media screen and (max-width: 1024px) {
  .project-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media screen and (max-width: 768px) {
  .project-grid {
    grid-template-columns: repeat(1, 1fr);
  }
}

@media screen and (max-width: 480px) {

  .project-grid {
    grid-template-columns: repeat(1, 1fr);
    gap: 20px;
  }
}

@media screen and (max-width: 320px) {

  
}
</style>