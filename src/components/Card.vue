<template>
  <article>
    <h3>{{idea.ideaTitle}}</h3>
    <p>{{idea.ideaBody}}</p>
    <button v-on:click="handleDelete">Delete</button>
  </article>
</template>

<script>
export default {
  name: 'Card',
  props: {
   idea: Object,
   deleteIdea: Function
  },
  methods: {
    handleDelete: function (event) {
      event.preventDefault()
      this.deleteIdea(this.idea.id)
    }
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

button {
  border: none;
  border-radius: none;
  outline: none;
  padding: 10px 20px;
}

</style>
