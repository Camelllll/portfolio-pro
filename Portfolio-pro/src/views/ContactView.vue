<template>
    <div class="contact-page">
      <h1>Contactez-moi</h1>
      <p>Si vous avez des questions ou souhaitez discuter d'un projet, n'hésitez pas à me contacter via le formulaire ci-dessous.</p>
      <form class="contact-form" @submit.prevent="submitForm">
        <div class="form-group">
          <label for="name">Nom</label>
          <input type="text" id="name" v-model="form.name" required>
        </div>
        <div class="form-group">
          <label for="email">Email</label>
          <input type="email" id="email" v-model="form.email" required>
        </div>
        <div class="form-group">
          <label for="message">Message</label>
          <textarea id="message" v-model="form.message" rows="5" required></textarea>
        </div>
        <button type="submit" class="submit-button">Envoyer</button>
      </form>
      <p v-if="messageSent" class="success-message">Message envoyé</p>
      <div class="social-media">
        <h3>Retrouvez-moi sur les réseaux sociaux</h3>
        <div class="social-icons">
          <a href="https://linkedin.com/in/votreprofil" target="_blank" class="social-icon">
            <img src="@/assets/img/logos/linkdin.svg" alt="LinkedIn">
          </a>
          <a href="https://github.com/votreprofil" target="_blank" class="social-icon">
            <img src="@/assets/img/logos/github.svg" alt="GitHub">
          </a>
        </div> <br>
        <h4>
            Site réalisé par Camélien Tournu, 2024 <br>    
            La simplicité est la sophistication.
        </h4>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        form: {
          name: '',
          email: '',
          message: ''
        },
        messageSent: false
      };
    },
    methods: {
      submitForm() {
        console.log('Nom:', this.form.name);
        console.log('Email:', this.form.email);
        console.log('Message:', this.form.message);
  
        this.messageSent = true;
  
        this.form.name = '';
        this.form.email = '';
        this.form.message = '';
  
        // Masquer le message après 3 secondes
        setTimeout(() => {
          this.messageSent = false;
        }, 3000);
      }
    }
  };
  </script>
  
  <style scoped>
  .contact-page {
    background-color: #fff;
    height: 250vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
  
    h1 {
      font-size: 36px;
      color: #000;
      margin-top: 830px;
    }
  
    p {
      font-size: 18px;
      color: #000;
      margin-bottom: 40px;
    }
  }
  
  .contact-form {
    width: 100%;
    max-width: 600px;
    display: flex;
    flex-direction: column;
    gap: 20px;
  }
  
  .form-group {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
  
    label {
      font-size: 16px;
      margin-bottom: 5px;
    }
  
    input, textarea {
      width: 100%;
      padding: 10px;
      font-size: 16px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
  }
  
  .submit-button {
    padding: 15px 30px;
    background-color: #7510f6;
    border: none;
    color: white;
    border-radius: 25px;
    cursor: pointer;
    transition: all 0.3s ease;
    font-family: 'Gilroy-Bold', sans-serif;
    font-weight: 400;
    font-size: 18px;
  
    &:hover {
      background-color: #37007f;
    }
  }
  
  .success-message {
    color: green;
    font-size: 18px;
    margin-top: 20px;
  }
  
  .social-media {
    background-color: #7510f6;
    width: 100%;
    height: 280px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin-top: 200px;
    gap: 20px;
  
    h3 {
      font-size: 18px;
      color: white;
    }
  
    h4 {
      font-size: 12px;
      color: white;
    }
  }
  
  .social-icons {
    display: flex;
    gap: 20px;
  }
  
  .social-icon {
    width: 50px;
    height: 50px;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: transparent;
    border: 2px solid white;
    border-radius: 50%;
    overflow: hidden;
    transition: all 0.3s ease;
  
    img {
      width: 50%;
      height: 50%;
      filter: invert(1);
    }
  
    &:hover {
      background-color: white;
      border-color: #7510f6;
  
      img {
        filter: invert(0);
      }
    }
  }

  .success-message {
    color: green;
    font-size: 18px;
    margin-top: 20px;
  }
  </style>