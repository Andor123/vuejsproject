<template>
  <div class="search">
    <h1>{{ title }}</h1>
    <form>
      <p>
        <label for="tv_name">TV station name:</label><br>
        <input type="text" name="tv_name" id="tv_name" v-model="name"/>
      </p>
      <p>Search result:</p>
      <div v-for="station in filteredStations">
        <p>{{ station.name }}</p>
      </div>
    </form>
  </div>
</template>

<script>
import json from '../assets/json/data.json'
export default {
  name: 'Search',
  data () {
    return {
      title: 'Search Engine',
      name: '',
      stations: json
    }
  },
  computed: {
    filteredStations() {
      return this.stations.filter(station => {
        return station.name.toLowerCase().indexOf(this.name.toLowerCase()) > -1
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
