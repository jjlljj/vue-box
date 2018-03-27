<template>
  <div class="cards-container" >
    <div v-for="idea in ideas">  
      <Card v-bind="{idea}"/>
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
    ideas: Array
  }
}
</script>

<style>

</style>
