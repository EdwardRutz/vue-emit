<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>The title is received from the App.vue via props.</p>
    <p>Props tell the child component to be ready to receive data to the parent along with specifying the data properties.</p>

  <button @click="printAdjective">Click Here</button>

  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  methods: {
    printAdjective() {

    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
p {
  text-align: left;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
