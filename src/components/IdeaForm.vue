<template>
  <form
    v-on:submit="handleSubmit"
    >
    <h1><span><img src="../assets/logo.png">ue</span>box</h1>
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
        const id = Date.now()
        const { ideaTitle, ideaBody } = this
        this.submitIdea({ ideaTitle, ideaBody, id })
      }
    }
  }
</script>

<style scoped>
img {
  height: 46px;
}

h1 {
  font-size: 42px;
  margin: 0 auto 10px;
}

input, button {
  box-sizing: border-box;
  display: block;
  height: 36px;
  margin: 20px auto;
  width: 240px;
}

input {
  padding-left: 10px;
}

button {
  background: #f2f2f2;
  border: none;
  border-radius: 0;
}

</style>
