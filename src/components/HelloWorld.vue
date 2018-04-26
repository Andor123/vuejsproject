<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>{{ msg2 }}</h2>
    <h2>{{ msg3 }}</h2>
    <div class="link">
      <router-link to="/form">Form</router-link>
      <router-link to="/list">List</router-link>
      <router-link to="/search">Search</router-link>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to My Vue.js Project',
      msg2: 'In this project we are going to have a TV form, a TV list and a search engine',
      msg3: 'Choose one of these options'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
</style>
