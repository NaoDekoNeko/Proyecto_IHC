<template>
  <div id="app">
    <header>
      <button @click="goBack" class="back-button">⬅️</button>
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
}

header h1 {
  margin: 0;
}

header .back-button {
  background: none;
  border: none;
  color: white;
  font-size: 24px;
  cursor: pointer;
  margin-right: 10px;
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
  padding: 10px;
  text-align: center;
}
</style>
