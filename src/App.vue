<template>
  <div id="app">
    <main>
      <router-view/>
    </main>
    <footer>
      <button @click="goToAbout">Conócenos</button>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'App'
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

main {
  flex: 1;
  display: flex;
  flex-direction: column;
}

footer {
  background: #42b983;
  color: white;
  text-align: center;
  padding: 10px;
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

</style>
