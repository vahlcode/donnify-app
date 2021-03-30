<template>
  <div id="app">
    <Tasks />
  </div>
</template>

<script>
import Tasks from './components/Tasks.vue'
export default {
  components: { Tasks },
}
</script>

<style>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

#app {
  font-family: "Poppins", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  background: #eff7ff;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  height: 100%;
  width: 100%;
  position: absolute;
}
</style>
