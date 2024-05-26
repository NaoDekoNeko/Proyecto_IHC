<template>
  <div class="login-container">
    <header>
      <button @click="goBack" class="back-button">⬅️</button>
      <h1>Autenticación</h1>
    </header>
    <div class="login-content">
      <div class="auth-section">
        <h2>Autenticación de usuario</h2>
        <p>Ingrese su correo electrónico para autenticarse en esta aplicación</p>
        <input type="email" placeholder="email@domain.com" v-model="email" />
        <input type="password" placeholder="******************" v-model="password" />
        <button @click="authenticate">Autenticar con e-mail</button>
        <p>o continuar con</p>
        <button class="google-button">Google</button>
        <button @click="goToSignup" class="signup-button">Crear una cuenta</button>
      </div>
      <div class="help-section">
        <p>
          ¡Hola de nuevo! Soy EVA, tu asistente virtual educativo. ¿Necesitas ayuda para iniciar sesión?
          No te preocupes, estoy aquí para ayudarte en cada paso del camino. Por favor, introduce tu correo
          y contraseña en los campos correspondientes y luego haz clic en 'Autenticar con e-mail' o por Google.
          Si aún no tienes una cuenta, puedes crear una haciendo clic en 'Crear una Cuenta' y seguir los sencillos
          pasos. ¡Estoy aquí para hacer que tu experiencia sea lo más fluida posible!
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Login',
  data() {
    return {
      email: '',
      password: ''
    };
  },
  methods: {
    goBack() {
      this.$router.push({ name: 'Home' });
    },
    authenticate() {
      // Lógica de autenticación
      console.log('Autenticando con email:', this.email);
      // Simula autenticación exitosa
      this.$router.push({ name: 'Courses' });
    },
    goToSignup() {
      this.$router.push({ name: 'Signup' });
    }
  }
}
</script>

<style scoped>
.login-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
  height: 100%;
  background-color: #e0f7fa;
}

header {
  display: flex;
  justify-content: flex-start;
  align-items: center;
  width: 100%;
  padding: 10px 20px;
  background: #42b983;
  color: white;
  box-sizing: border-box;
  position: fixed;
  top: 0;
  left: 0;
}

.back-button {
  background: none;
  border: none;
  color: white;
  font-size: 24px;
  cursor: pointer;
  margin-right: 10px;
}

h1 {
  margin: 0;
  font-size: 24px;
}

.login-content {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  width: 80%;
  margin-top: 80px; /* Ajusta esto según la altura del header */
}

.auth-section, .help-section {
  flex: 1;
  margin: 0 20px;
  background-color: #f5f5f5;
  padding: 20px;
  border-radius: 10px;
}

.auth-section {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.auth-section h2 {
  margin-bottom: 10px;
}

.auth-section input {
  width: 100%;
  padding: 10px;
  margin: 10px 0;
  border: 1px solid #ccc;
  border-radius: 5px;
}

.auth-section button {
  width: 100%;
  padding: 10px;
  background-color: #000;
  color: #fff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  margin: 10px 0;
}

.auth-section button:hover {
  background-color: #333;
}

.google-button {
  background-color: #4285f4;
}

.signup-button {
  background-color: #42b983;
}

.help-section {
  background-color: #333;
  color: #fff;
  padding: 20px;
  border-radius: 10px;
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
