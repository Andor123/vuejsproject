<template>
    <div class="form">
      <h1>TV Form</h1>
      <form @submit="submit" method="post" action="" name="form" id="form">
        <p>
          <label for="name">TV station name:</label><br>
          <input type="text" name="name" id="name" v-model="name"/>
        </p>
        <p>
          <label for="country">TV station country:</label><br>
          <input type="text" name="country" id="country" v-model="country"/>
        </p>
        <p>
          <label for="year">TV station launch year:</label><br>
          <input type="number" name="year" id="year" v-model="year"/>
        </p>
        <p>
          <input type="submit" value="Submit"/>
        </p>
      </form>
    </div>
</template>

<script>
  export default {
    name: "Form",
    data () {
      return {
        name: '',
        country: '',
        year: 0
      }
    },
    methods: {
      submit: function (e) {
        if (this.name !== '' && this.country !== '' && this.year !== 0)
          alert("TV station name: " + this.name +
            "\nTV station country: " + this.country +
            "\nTV station launch year: " + this.year);
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
input[type="submit"] {
  border-color: black;
  color: black;
  background-color: white;
}
</style>
