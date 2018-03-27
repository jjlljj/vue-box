<template>
  <article>
    <h3>{{idea.ideaTitle}}</h3>
    <p>{{idea.ideaBody}}</p>
  </article>
</template>

<script>
export default {
  name: 'Card',
  props: {
   idea: Object
  }
}
</script>

<style>

</style>
