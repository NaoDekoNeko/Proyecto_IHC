<template>
  <div class="signup-container">
    <header>
      <button @click="goBack" class="back-button">⬅️</button>
      <h1>Registro</h1>
    </header>
    <div class="signup-content">
      <div class="auth-section">
        <h2>Crea una cuenta</h2>
        <p>Ingrese su correo electrónico para registrarse en esta aplicación</p>
        <input type="email" placeholder="email@domain.com" v-model="email" />
        <input type="password" placeholder="******************" v-model="password" />
        <button @click="register">Crear con e-mail</button>
        <p>o continuar con</p>
        <button class="google-button">Google</button>
        <button @click="goToLogin" class="login-button">Iniciar Sesión</button>
      </div>
      <div class="help-section">
        <p>
          ¡Hola! ¿Quieres crear una cuenta? ¡Es muy fácil! Solo ingresa tu dirección de correo electrónico y luego haz clic en 'Crear con e-mail'.
          Te enviaremos un correo electrónico con los detalles de tu nueva cuenta, incluida tu contraseña. ¿Prefieres entrar con Google? ¡Sin problema!
          Simplemente haz clic en 'Google' y estarás listo para empezar. ¡Espero que disfrutes de tu experiencia en nuestra plataforma!
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Signup',
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
    register() {
      // Lógica de registro
      console.log('Registrando con email:', this.email);
      // Simula registro exitoso
      this.$router.push({ name: 'Courses' });
    },
    goToLogin() {
      this.$router.push({ name: 'Login' });
    }
  }
}
</script>

<style scoped>
.signup-container {
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

.signup-content {
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

.login-button {
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
