<template>
  <div class="search">
    <h1>{{ title }}</h1>
    <form>
      <p>
        <label for="tv_name">TV station name:</label><br>
        <input type="text" name="tv_name" id="tv_name" v-model="name"/>
      </p>
      <p>
        <button type="button" v-on:click="search()">Search</button>
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
    search: function () {
      console.log({name: this.name})
      return this.stations.filter((station) => {
        return station.name.match(this.name)
      })
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
button {
  border-color: black;
  color: black;
  background-color: white;
}
</style>
