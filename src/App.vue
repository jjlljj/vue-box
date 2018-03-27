<template>
  <div id="app">
    <section class="input-section">
      <IdeaForm v-bind:submitIdea="submitIdea"/>
    </section>
    <section class="cards-section">
    </section>
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
body {
  margin: 0;
  padding: 0;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 0;
}

.input-section {
  background: #cfdde6;
  padding: 60px 0 20px;
}
</style>
