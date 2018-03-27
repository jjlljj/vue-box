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

<style scoped>
article {
  background: #f2f2f2;
  width: 300px;
  height: auto;
  margin: 20px auto;
  padding: 20px;
}

</style>
