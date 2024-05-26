<template>
  <div class="courses-container">
    <header>
      <div class="left-section">
        <button @click="goBack" class="back-button">⬅️</button>
        <h1>Mis Cursos</h1>
      </div>
      <div class="profile">
        <img :src="user.profilePic" alt="Profile Picture" class="profile-pic" @click="toggleMenu"/>
        <div v-if="menuOpen" class="profile-menu">
          <p>{{ user.name }}</p>
          <button @click="goToSettings">Configuración</button>
        </div>
      </div>
    </header>
    <main>
      <div v-if="courses.length === 0" class="no-courses">
        <p>No tienes cursos aún. ¡Añade un curso para empezar!</p>
        <button @click="addCourse">Añadir Curso</button>
      </div>
      <div v-else class="courses-list">
        <div v-for="course in courses" :key="course.id" class="course-item">
          <h2>{{ course.name }}</h2>
        </div>
      </div>
    </main>
  </div>
</template>

<script>
export default {
  name: 'Courses',
  data() {
    return {
      user: {
        name: 'Nombre del Usuario',
        profilePic: require('@/assets/img/user-profile-icon.jpg')
      },
      courses: [],
      menuOpen: false
    };
  },
  methods: {
    toggleMenu() {
      this.menuOpen = !this.menuOpen;
    },
    goToSettings() {
      // Lógica para ir a la configuración del usuario
    },
    addCourse() {
      const newCourse = { id: Date.now(), name: 'Nuevo Curso' };
      this.courses.push(newCourse);
    },
    goToAbout() {
      // Lógica para ir a la página de Conócenos
    },
    goBack() {
      this.$router.push({ name: 'Home' });
    }
  }
};
</script>

<style scoped>
.courses-container {
  display: flex;
  flex-direction: column;
  height: 100vh;
  background-color: #e0f7fa;
}

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px 20px;
  background: #42b983;
  color: white;
  width: 100%;
  box-sizing: border-box;
}

.left-section {
  display: flex;
  align-items: center;
  width: 100%;
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
  flex-grow: 1;
}

.profile {
  position: relative;
  display: flex;
  align-items: center;
}

.profile-pic {
  border-radius: 50%;
  width: 50px;
  cursor: pointer;
}

.profile-menu {
  position: absolute;
  top: 60px;
  right: 0;
  background: white;
  color: black;
  padding: 10px;
  border-radius: 5px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}

main {
  flex: 1;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 20px;
}

.no-courses {
  text-align: center;
}

.courses-list {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
}

.course-item {
  background: white;
  padding: 20px;
  border-radius: 5px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}

button:hover {
  background: #333;
}
</style>
