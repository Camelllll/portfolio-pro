<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <div class="wrapper">
      <RouterLink to="/">
        <img src="@/assets/img/camel.png" alt="logo" class="logo" />
      </RouterLink>
      <nav class="navbar">
        <RouterLink to="/">Accueil</RouterLink>
        <RouterLink to="/about">À Propos</RouterLink>
        <RouterLink to="/projects">Projets</RouterLink>
        <RouterLink to="/contact">Contact</RouterLink>
      </nav>
    </div>
  </header>
  <main class="centered">
    <h1>Développeur Web Full Stack</h1>
    <h2>Passionné par le développement web et les nouvelles technologies</h2>
  </main>
</template>

<style scoped lang="scss">
.wrapper {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: -50px;
}

.logo {
  height: 150px;
  margin-right: 800px;
  margin-left: -40px;
}

.centered {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 60vh;
  text-align: center;
}

.navbar {
  display: flex;
  gap: 40px; 
  margin-left: 90px;

  a {
    text-decoration: none;
    color: #000;
    font-size: 16px;
    font-weight: 500;
    transition: all 0.3s ease;

    &:hover {
      color: #f00;
    }
  }
}
</style>