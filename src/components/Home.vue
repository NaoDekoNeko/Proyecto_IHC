<template>
  <div class="home-container">
    <h1>Educational Virtual Assistant</h1>

    <div class="buttons">
      <button @click="goToLogin">Iniciar Sesión</button>
      <button @click="goToSignup">Crear cuenta</button>
    </div>
    <div class="welcome-message">
      <p>
        ¡Hola! Soy EVA, tu asistente virtual educativo. Estoy aquí para ayudarte a navegar por nuestra plataforma y sacar el máximo provecho de tu experiencia de aprendizaje. ¿Listo para empezar? Simplemente dale al botón de 'Iniciar Sesión' si ya tienes una cuenta o 'Crear Cuenta' si eres nuevo aquí. ¡Estoy emocionado de acompañarte en tu viaje de aprendizaje!
      </p>
    </div>
    <div class="aboutus-container">
      <button @click="goToAboutUs">Sobre Nosotros</button>
    </div>
    <div class="robot">
      <img src="../assets/images/image_19.png" alt="Robot">
    </div>
  </div>
</template>

<script>
export default {
  name: 'Home',
  methods: {
    goToLogin() {
      this.$router.push({ name: 'Login' });
    },
    goToSignup() {
      this.$router.push({ name: 'Signup' });
    },
    goToAboutUs() {
      this.$router.push({ name: 'AboutUs' });
    }
  }
}
</script>

<style scoped>
html, body {
  height: 100%;
  margin: 0;
  font-family: 'Inter', sans-serif;
}

.home-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: 100%;
  background-color: #D6FFFF;
  position: relative;
}

h1 {
  font-size: 24px;
  margin-bottom: 20px;
}

.welcome-message {
  color: #fff;
  border-radius: 16px 16px 0 16px;
  background: #000000;
  margin: 0 0 88px 60.2px;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 20px;
  box-sizing: border-box;
  font-weight: 500;
  font-size: 20px;
  max-width: 80%;
  text-align: center;
}

.robot img {
  width: 200px; /* Cambiado de 150px a 200px */
  height: 200px; /* Cambiado de auto a 200px */
}

.robot {
  position: absolute;
  bottom: 50px;
  right: 50px;
  width: 150px;
  height: auto;
}

.buttons {
  display: flex;
  gap: 20px;
  margin-bottom: 20px;
}

.aboutus-container {
  position: absolute;
  bottom: 10px;
  left: 10px;
  font-size: 1.5rem;
}

button {
  padding: 10px 20px;
  border: none;
  border-radius: 10px;
  background-color: #000;
  color: #fff;
  font-size: 16px;
  cursor: pointer;
}

button:hover {
  background-color: #333;
}
</style>
