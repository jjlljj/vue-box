<template>
  <div class="cards-container" >
    <div v-for="idea in ideas">  
      <Card v-bind="{idea, deleteIdea}"/>
    </div>
  </div>
</template>

<script>
import Card from './Card.vue'

export default {
  name: 'IdeaCards',
  components: {
    Card
  },
  props: {
    ideas: Array,
    deleteIdea: Function
  }
}
</script>

<style>

</style>
