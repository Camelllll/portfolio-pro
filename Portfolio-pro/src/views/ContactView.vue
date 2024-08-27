<template>
  <div class="contact-page">
    <div class="margin-project">
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
      </div>
      <br>
      <h4>Site réalisé par Camélien Tournu, 2024 <br> La simplicité est la sophistication.</h4>
    </div>
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
  padding: 20px;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  min-height: 100vh;
}

.margin-project {
  margin-top: 100vh;
}

h1 {
  font-size: 2.5rem;
  margin-bottom: 20px;
}

p {
  font-size: 1.125rem;
  margin-bottom: 40px;
}

.contact-form {
  width: 100%;
  max-width: 600px;
  display: flex;
  flex-direction: column;
  gap: 20px;
  margin: auto;
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
}

.submit-button:hover {
  background-color: #37007f;
}

.success-message {
  color: green;
  font-size: 18px;
  margin-top: 20px;
}

.social-media {
  background-color: #7510f6;
  width: 100%;
  padding: 40px 20px;
  margin-top: 50px;
  text-align: center;
}

h3 {
  font-size: 18px;
  color: white;
  margin-bottom: 20px;
}

h4 {
  font-size: 12px;
  color: white;
}

.social-icons {
  display: flex;
  justify-content: center;
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

@media (max-width: 768px) {
  h1 {
    font-size: 2rem;
  }

  p {
    font-size: 1rem;
  }

  .submit-button {
    font-size: 16px;
    padding: 12px 25px;
  }

  .social-media {
    padding: 30px 15px;
  }

  h3 {
    font-size: 16px;
  }
}

@media (max-width: 480px) {
  h1 {
    font-size: 1.75rem;
  }

  p {
    font-size: 0.875rem;
  }

  .submit-button {
    font-size: 14px;
    padding: 10px 20px;
  }

  .social-media {
    padding: 20px 10px;
  }

  h3 {
    font-size: 14px;
  }

  .social-icon {
    width: 40px;
    height: 40px;

    img {
      width: 50%;
      height: 50%;
    }
  }
}
</style>
