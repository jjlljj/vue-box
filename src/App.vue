<template>
  <div id="app">
    <img src="./assets/logo.png">
    <IdeaForm v-bind:submitIdea="submitIdea"/>
  </div>
</template>

<script>
import IdeaForm from './components/IdeaForm.vue'

export default {
  name: 'app',
  components: {
    IdeaForm
  },
  data () {
    return {
      ideas: []
    }
  },
  methods: {
    submitIdea (idea) {
      console.log('yo')
      console.log(idea)
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
