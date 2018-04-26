<template>
  <div class="form">
    <h1>{{ title }}</h1>
    <form @submit="submit" name="form" id="form">
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
        <input type="submit" value="Submit"/>
      </p>
    </form>
  </div>
</template>

<script>
import json from './json/data.json'
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
    submit: function (e) {
      if (this.id !== 0 && this.name !== '' && this.country !== '' && this.lYear !== 0 && this.dYear !== '') {
        this.$set(this.stations, this.stations.id, this.id)
        this.$set(this.stations, this.stations.name, this.name)
        this.$set(this.stations, this.stations.country, this.country)
        this.$set(this.stations, this.stations.lYear, this.lYear)
        this.$set(this.stations, this.stations.dYear, this.dYear)
      }
      e.preventDefault();
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
