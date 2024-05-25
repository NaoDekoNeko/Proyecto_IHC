<template>
  <div class="home-container">
    <h1>Educational Virtual Assistant</h1>
    <div class="welcome-message">
      <p>
        ¡Hola! Soy EVA, tu asistente virtual educativo. Estoy aquí para ayudarte a navegar por nuestra plataforma y sacar el máximo provecho de tu experiencia de aprendizaje. ¿Listo para empezar? Simplemente dale al botón de 'Iniciar Sesión' si ya tienes una cuenta o 'Crear Cuenta' si eres nuevo aquí. ¡Estoy emocionado de acompañarte en tu viaje de aprendizaje!
      </p>
    </div>
    <div class="buttons">
      <button @click="goToLogin">Iniciar Sesión</button>
      <button @click="goToSignup">Crear cuenta</button>
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
    }
  }
}
</script>

<style scoped>
.home-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: 100%;
  background-color: #e0f7fa;
}

h1 {
  font-size: 24px;
  margin-bottom: 20px;
}

.welcome-message {
  background-color: #000;
  color: #fff;
  padding: 20px;
  border-radius: 10px;
  text-align: center;
  max-width: 600px;
  margin-bottom: 20px;
}

.buttons {
  display: flex;
  gap: 20px;
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
