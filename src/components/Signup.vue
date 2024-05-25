<template>
  <div class="login-container">
    <div class="login-content">
      <div class="auth-section">
        <p>Ingrese su correo electrónico para registrarse en esta aplicación</p>
        <input type="email" placeholder="email@domain.com" v-model="email" />
        <button @click="register">crear con e-mail</button>
        <p>o continuar con</p>
        <button class="google-button">Google</button>
        <button @click="goToLogin" class="login-button">Iniciar Sesión</button>
        <p class="terms">
          Al hacer clic en Continuar acepta nuestros
          <a href="#">Términos de servicio</a> y
          <a href="#">Política de privacidad</a>
        </p>
      </div>
      <div class="help-section">
        <p>
          ¡Hola! ¿Quieres crear una cuenta? ¡Es muy fácil! Solo ingresa tu dirección de correo electrónico y luego haz clic en 'Crear con e-mail'. Te enviaremos un correo electrónico con los detalles de tu nueva cuenta, incluida tu contraseña. ¿Prefieres entrar con Google? ¡Sin problema! Simplemente haz clic en 'Google' y estarás listo para empezar. ¡Espero que disfrutes de tu experiencia en nuestra plataforma!
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
      email: ''
    };
  },
  methods: {
    goBack() {
      this.$router.push({ name: 'Home' });
    },
    register() {
      // Lógica de registro
      console.log('Registrando con email:', this.email);
    },
    goToLogin() {
      this.$router.push({ name: 'Login' });
    }
  }
}
</script>

<style scoped>
.login-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: 100%;
  background-color: #e0f7fa;
}

.login-content {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  width: 80%;
  margin-top: 20px;
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

.terms {
  font-size: 12px;
  color: #666;
  text-align: center;
}

.terms a {
  color: #000;
  text-decoration: none;
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
