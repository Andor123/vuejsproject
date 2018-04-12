<template>
  <div class="list">
    <h1>TV List</h1>
    <paginate
      name="channels"
      :list="stations"
      :per="100"
    >
    <table border="1" align="center">
      <tr>
        <th>Name</th>
        <th>Country</th>
        <th>Launch Year</th>
        <th>Defunct Year</th>
      </tr>
      <tr v-for="station in paginated('channels')">
        <td>{{station.name}}</td>
        <td>{{station.country}}</td>
        <td>{{station.lYear}}</td>
        <td>{{station.dYear}}</td>
      </tr>
    </table>
    </paginate>
    <paginate-links
      for="channels"
      :show-step-links="true"
      style="
      list-style-type: none;
      padding: 0;
      margin: 0;
      cursor: pointer;
      color: black;
      display: inline-block;"
    >
    </paginate-links>
  </div>
</template>

<script>
import json from './json/data.json'
export default {
  name: 'List',
  data () {
    return {
      stations: json,
      paginate: ['channels']
    }
  }
}
</script>

<style scoped>
h1 {
  font-weight: normal;
}
table, tr, th, td {
  border-collapse: collapse;
}
</style>
