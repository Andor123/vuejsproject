<template>
  <div class="search">
    <h1>{{ title }}</h1>
    <form @submit="search" name="search" id="search">
      <p>
        <label for="tv_name">TV station name:</label><br>
        <input type="text" name="tv_name" id="tv_name" v-model="name"/>
      </p>
      <p>
        <input type="submit" value="Submit"/>
      </p>
    </form>
  </div>
</template>

<script>
import json from './json/data.json'
export default {
  name: 'Search',
  data () {
    return {
      title: 'Search Engine',
      name: '',
      stations: json
    }
  },
  methods: {
    search: function (e) {
      if (this.name !== '') {
        this.$set(this.stations, this.stations.name, this.name)
      }
      e.preventDefault()
    }
  }
}
</script>

<style scoped>
h1 {
  font-weight: normal;
}
label {
  font-weight: bold;
}
input[type='submit'] {
  border-color: black;
  color: black;
  background-color: white;
}
</style>
