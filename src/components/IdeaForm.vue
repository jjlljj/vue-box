<template>
  <form
    v-on:submit="handleSubmit"
    >
    <h1><span>Vue</span>box</h1>
    <input
      type="text"
      placeholder="Title"
      v-model="ideaTitle"
      />
    <input
      type="text"
      placeholder="Body"
      v-model="ideaBody"
      />
    <button>Submit</button>
  </form>
</template>

<script>
  export default {
    name: 'IdeaForm',
    props: {
      submitIdea: Function
    },
    data () {
      return {
        ideaTitle: '',
        ideaBody: ''
      }
    },
    methods: {
      handleSubmit: function (event) {
        event.preventDefault()
        const { ideaTitle, ideaBody } = this
        this.submitIdea({ ideaTitle, ideaBody })
      }
    }
  }
</script>

<style scoped>
input, button {
  box-sizing: border-box;
  display: block;
  height: 36px;
  margin: 20px auto;
  width: 240px;
}

button {
  background: #f2f2f2;
  border-radius: 0;
}
</style>
