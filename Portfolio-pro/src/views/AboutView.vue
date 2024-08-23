<template>
  <div class="profile">
    <div class="profil-txt"> <br> <br>
    <h1>Moi c'est Camélien, Ravi de te rencontrer !</h1> <br>
    <p>
      Salut ! je suis étudiant en BUT Métier du Multimédia et de l'internet, et très prochainement à l'ESGI
      pour faire de la Cyber Sécurité ! Passionné par le développement web et les nouvelles technologies, je suis
      toujours à la recherche de nouveaux projets à réaliser. J'aime apprendre de nouvelles choses et partager mes
      connaissances avec les autres. Je suis également un grand fan de jeux vidéo et de musique.
    </p>
  </div>
    <div class="big-section">
      <div class="flex">
        <section class="section">
          <div class="image-container">
            <img src="@/assets/img/developpement.png" alt="Icon">
          </div>
          <h2>Back-End</h2>
          <p>
            Passionné par la création de systèmes robustes et efficaces.
          </p> <br>
          <h3>Langages que j'utilise :</h3>
          <p>Python</p>
          <p>Java</p>
          <p>Node.js</p>
          <p>PHP</p>
          <p>Filament PHP</p> <br>
          <h3>Frameworks que j'utilise :</h3>
          <p>Symfony</p>
          <p>Laravel</p>
        </section>

        <section class="section">
        <div class="card">
          <div class="image-container">
            <img src="@/assets/img/developpeur.png" alt="Icon">
          </div>
          <h2>Front-End</h2>
          <p>
            Passionné par la création d'interfaces utilisateur attrayantes et fonctionnelles.
          </p> <br>
          <h3>Langages que j'utilise :</h3>
          <p>HTML</p>
          <p>CSS</p>
          <p>JavaScript</p>
          <p>React native</p>
          <p>Vue.js</p> <br>
          <h3>CMS que j'utilise :</h3>
          <p>WordPress</p>
          <p>Webflow</p>
          </div>
        </section>

        <section class="section">
          <div class="image-container">
            <img src="@/assets/img/chef-de-projet.png" alt="Icon">
          </div>
          <h2>Chef de Projet</h2>
          <p>
            Passionné par la coordination d'équipes et la réalisation de projets de développement.
          </p> <br>
          <h3>Compétences en gestion de projet :</h3>
          <p>Gestion d'équipe</p>
          <p>Planification de projet</p>
          <p>Gestion des risques</p>
          <p>Communication interne</p>
          <h3>Outils que j'utilise :</h3>
          <p>Asana</p>
          <p>Trello</p>
          <p>Microsoft Project</p>
          <p>Slack</p>
        </section>
      </div>
    </div>

  </div>
</template>

<style scoped>

.big-section {
  border-radius: 20px 20px 20px 20px;
  box-shadow: 0 0 20px 0 rgba(0, 0, 0, 0.1);
  overflow: hidden;
  margin-right: 50px;
  margin-left: 50px;
  margin-top: 100px;
  position: relative;
  z-index: 1;
}

.flex {
  display: flex;
  justify-content: space-between;
  gap: 0; 
}

.section {
  width: 33.33%; 
  height: 600px;
  padding: 20px;
  border: 0.2px solid #ebebeb;
  background-color: #ffffff;
  position: relative;
  z-index: 2;
  font-family: "europa", sans-serif;

  h2 {
    font-size: 20px;
    color: #000000;
    margin-top: 10px;
    font-weight: 600;
  }

  p {
    font-size: 16px;
    color: #000000;
    margin-top: 10px;
  }

  h3 {
    font-size: 16px;
    color: #7510f6;
    font-weight: 600;
    text-decoration: underline;
    margin-top: 10px;
  }

  img {
    width: 30px;
    height: 30px;
  }
}

.image-container {
  width: 70px; 
  height: 70px;
  border-radius: 50%;
  background-color: #5BE9B9;
  display: flex;
  margin-left: 43%;
  margin-bottom: 40px;
  align-items: center;
  justify-content: center;
  overflow: hidden;
}

.image-container img {
  width: 30px;
  height: 30px;
}

.profil-txt {
  padding: 120px;
  border-radius: 0 0 20px 20px;
  margin: 0 40px;

  h1 {
    font-size: 30px;
    color: white;
  }

  p {
    font-size: 19px;
    color: white;
    margin-top: 10px;
    margin-left: 100px;
    margin-right: 100px;
    font-weight: 400;
    font-family: "europa", sans-serif;
    line-height: 1.5;
  }
}
</style>