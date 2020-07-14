<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/codingdojo.png">
    <SurveyDojo msg="Please complete the following survey"/>
  </div>
</template>

<script>
import SurveyDojo from './components/SurveyDojo.vue'

export default {
  name: 'App',
  components: {
    SurveyDojo
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #000000;
  margin: auto;
  padding: 20px;
  width: 600px;
}
</style>
