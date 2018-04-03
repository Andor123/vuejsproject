<template>
  <div class="list">
    <h1>TV List</h1>
    <table border="1" align="center">
      <tr>
        <th>Name</th>
        <th>Country</th>
        <th>Launch Year</th>
        <th>Defunct Year</th>
      </tr>
      <tr v-for="station in stations">
        <td>{{station.name}}</td>
        <td>{{station.country}}</td>
        <td>{{station.lYear}}</td>
        <td>{{station.dYear}}</td>
      </tr>
    </table>
  </div>
</template>

<script>
  export default {
    name: "List",
    data() {
      return {
        stations: [
          { name: 'W1XAY', country: 'United States of America', lYear: 1928, dYear: 1930 },
          { name: 'W2XB', country: 'United States of America', lYear: 1928, dYear: 1942 },
          { name: 'W2XBS', country: 'United States of America', lYear: 1928, dYear: 1941 },
          { name: 'W3XK', country: 'United States of America', lYear: 1928, dYear: 1934 },
          { name: 'VE9EC', country: 'Canada', lYear: 1931, dYear: 1935 },
          { name: 'W2XAB', country: 'United States of America', lYear: 1931, dYear: 1941 },
          { name: 'Fernsehsender Paul Nipkow', country: 'Germany', lYear: 1935, dYear: 1944 },
          { name: 'TF1', country: 'France', lYear: 1935, dYear: 'Ongoing' },
          { name: 'BBC London', country: 'United Kingdom', lYear: 1936, dYear: 'Ongoing' },
          { name: 'BBC One', country: 'United Kingdom', lYear: 1936, dYear: 'Ongoing' },
          { name: 'Petersburg - Channel 5', country: 'Russia', lYear: 1938, dYear: 'Ongoing' },
          { name: 'Soviet Central Television', country: 'Soviet Union (Russia)', lYear: 1938, dYear: 1991 },
          { name: 'WBBM-TV', country: 'United States of America', lYear: 1940, dYear: 'Ongoing' },
          { name: 'KYW-TV', country: 'United States of America', lYear: 1941, dYear: 'Ongoing' },
          { name: 'WCBS-TV', country: 'United States of America', lYear: 1941, dYear: 'Ongoing' },
          { name: 'WNBC', country: 'United States of America', lYear: 1941, dYear: 'Ongoing' },
          { name: 'WRGB', country: 'United States of America', lYear: 1942, dYear: 'Ongoing' },
          { name: 'British Forces Broadcasting Service', country: 'United Kingdom', lYear: 1943, dYear: 'Ongoing' },
          { name: 'WNYW', country: 'United States of America', lYear: 1944, dYear: 'Ongoing' },
          { name: 'DuMont Television Network', country: 'United States of America', lYear: 1946, dYear: 1956 },
          { name: 'Südwestfunk', country: 'Germany', lYear: 1946, dYear: 1998 }
        ]
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
