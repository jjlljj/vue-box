<template>
  <div id="app">
    <section class="input-section">
      <IdeaForm v-bind:submitIdea="submitIdea"/>
    </section>
    <section class="cards-section">
      <IdeaCards v-if="ideas" v-bind:ideas="ideas" v-bind:deleteIdea="deleteIdea" />
    </section>
  </div>
</template>

<script>
import IdeaForm from './components/IdeaForm.vue'
import IdeaCards from './components/IdeaCards.vue'

export default {
  name: 'app',
  components: {
    IdeaForm,
    IdeaCards
  },
  data () {
    return {
      ideas: []
    }
  },
  methods: {
    submitIdea (idea) {
      console.log(idea)
      this.ideas.push(idea)
    },
    deleteIdea (id) {
      this.ideas = this.ideas.filter(idea => idea.id !== id)
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
