<template>
  <form
    v-on:submit="submitIdea()"
    >
    <h1><span>Vue</span>box</h1>
    <input
      type="text"
      />
  </form>
</template>

<script>
  export default {
    name: 'IdeaForm',
    props: {
      submitIdea: Function
    }
  }
</script>

<style scoped>

</style>
