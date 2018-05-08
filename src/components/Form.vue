<template>
  <div class="form">
    <h1>{{ title }}</h1>
    <form>
      <p>
        <label for="id">TV ID:</label><br>
        <input type="number" class="form-control" name="id" id="id" v-model="id"/>
      </p>
      <p>
        <label for="name">TV station name:</label><br>
        <input type="text" class="form-control" name="name" id="name" v-model="name"/>
      </p>
      <p>
        <label for="country">TV station country:</label><br>
        <input type="text" class="form-control" name="country" id="country" v-model="country"/>
      </p>
      <p>
        <label for="lYear">TV station launch year:</label><br>
        <input type="number" class="form-control" name="lYear" id="lYear" v-model="lYear"/>
      </p>
      <p>
        <label for="dYear">TV station defunct year:</label><br>
        <input type="text" class="form-control" name="dYear" id="dYear" v-model="dYear"/>
      </p>
      <p>
        <button type="button" v-on:click="submit()">Submit</button>
      </p>
    </form>
  </div>
</template>

<script>
import json from '../assets/json/data.json'
export default {
  name: 'Form',
  data () {
    return {
      title: 'TV Form',
      id: 0,
      name: '',
      country: '',
      lYear: 0,
      dYear: '',
      stations: json
    }
  },
  methods: {
    submit: function () {
      this.stations.push({id: this.id, name: this.name, country: this.country, lYear: this.lYear, dYear: this.dYear})
      console.log({id: this.id, name: this.name, country: this.country, lYear: this.lYear, dYear: this.dYear})
      const data = JSON.stringify(this.stations)
      window.localStorage.setItem('stations', data)
      console.log(JSON.parse(window.localStorage.getItem('stations')))
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
