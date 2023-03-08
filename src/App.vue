<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="TOngoa soa eto am ny VUe.Js"/>
    <FormComponent/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import FormComponent from './components/FormComponent.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    FormComponent
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
