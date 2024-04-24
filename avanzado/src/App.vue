<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <Formulario_registro></Formulario_registro>
</template>

<script>
import Formulario_registro from './components/Formulario_registro.vue'

export default {
  name: 'App',
  components: {
    Formulario_registro
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
