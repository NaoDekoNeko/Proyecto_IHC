<template>
  <div id="app">
    <header>
      <button @click="goBack" class="image-10"></button>
      <h1>Educational Virtual Assistant</h1>
    </header>
    <main>
      <router-view/>
    </main>
    <footer>
      <p>Educational Virtual Assistant (EVA 1.0)</p>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'App',
  methods: {
    goBack() {
      this.$router.push({ name: 'Home' });
    }
  }
}
</script>

<style>
html, body, #app {
  height: 100%;
  margin: 0;
  background-color: #e0f7fa;
}

#app {
  display: flex;
  flex-direction: column;
}

header {
  background: #42b983;
  color: white;
  padding: 20px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: 30px; 
}

header h1 {
  margin: 0;
}

header .image-10 {
  box-shadow: 0px 4px 4px 0px rgba(0, 0, 0, 0.25);
  background: url('assets/images/image_10.png') 50% / cover no-repeat;
  margin-bottom: 69.5px;
  align-self: flex-start;
  width: 30px; /* Cambiado de 50px a 100px */
  height: 30px; /* Cambiado de 50px a 100px */
}

main {
  flex: 1;
  display: flex;
  align-items: center;
  justify-content: center;
}

footer {
  background: #42b983;
  color: white;
  padding: 5px;
  text-align: center;
  
  
}
</style>
