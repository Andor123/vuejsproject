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
      <tr v-for="station in stations" v-bind:key="station.id">
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
  name: 'List',
  data () {
    return {
      stations: [
        { id: 1, name: 'W1XAY', country: 'United States of America', lYear: 1928, dYear: 1930 },
        { id: 2, name: 'W2XB', country: 'United States of America', lYear: 1928, dYear: 1942 },
        { id: 3, name: 'W2XBS', country: 'United States of America', lYear: 1928, dYear: 1941 },
        { id: 4, name: 'W3XK', country: 'United States of America', lYear: 1928, dYear: 1934 },
        { id: 5, name: 'VE9EC', country: 'Canada', lYear: 1931, dYear: 1935 },
        { id: 6, name: 'W2XAB', country: 'United States of America', lYear: 1931, dYear: 1941 },
        { id: 7, name: 'Fernsehsender Paul Nipkow', country: 'Germany', lYear: 1935, dYear: 1944 },
        { id: 8, name: 'TF1', country: 'France', lYear: 1935, dYear: 'Ongoing' },
        { id: 9, name: 'BBC London', country: 'United Kingdom', lYear: 1936, dYear: 'Ongoing' },
        { id: 10, name: 'BBC One', country: 'United Kingdom', lYear: 1936, dYear: 'Ongoing' },
        { id: 11, name: 'Petersburg - Channel 5', country: 'Russia', lYear: 1938, dYear: 'Ongoing' },
        { id: 12, name: 'Soviet Central Television', country: 'Soviet Union (Russia)', lYear: 1938, dYear: 1991 },
        { id: 13, name: 'WBBM-TV', country: 'United States of America', lYear: 1940, dYear: 'Ongoing' },
        { id: 14, name: 'KYW-TV', country: 'United States of America', lYear: 1941, dYear: 'Ongoing' },
        { id: 15, name: 'WCBS-TV', country: 'United States of America', lYear: 1941, dYear: 'Ongoing' },
        { id: 16, name: 'WNBC', country: 'United States of America', lYear: 1941, dYear: 'Ongoing' },
        { id: 17, name: 'WRGB', country: 'United States of America', lYear: 1942, dYear: 'Ongoing' },
        { id: 18, name: 'British Forces Broadcasting Service', country: 'United Kingdom', lYear: 1943, dYear: 'Ongoing' },
        { id: 19, name: 'WNYW', country: 'United States of America', lYear: 1944, dYear: 'Ongoing' },
        { id: 20, name: 'DuMont Television Network', country: 'United States of America', lYear: 1946, dYear: 1956 },
        { id: 21, name: 'Südwestfunk', country: 'Germany', lYear: 1946, dYear: 1998 },
        { id: 22, name: 'KSDK', country: 'United States of America', lYear: 1947, dYear: 'Ongoing' },
        { id: 23, name: 'KTLA', country: 'United States of America', lYear: 1947, dYear: 'Ongoing' },
        { id: 24, name: 'WDIV-TV', country: 'United States of America', lYear: 1947, dYear: 'Ongoing' },
        { id: 25, name: 'WEWS-TV', country: 'United States of America', lYear: 1947, dYear: 'Ongoing' },
        { id: 26, name: 'WJLA-TV', country: 'United States of America', lYear: 1947, dYear: 'Ongoing' },
        { id: 27, name: 'WMAR-TV', country: 'United States of America', lYear: 1947, dYear: 'Ongoing' },
        { id: 28, name: 'WPVI-TV', country: 'United States of America', lYear: 1947, dYear: 'Ongoing' },
        { id: 29, name: 'WRC-TV', country: 'United States of America', lYear: 1947, dYear: 'Ongoing' },
        { id: 30, name: 'WTMJ-TV', country: 'United States of America', lYear: 1947, dYear: 'Ongoing' },
        { id: 31, name: 'WTTG', country: 'United States of America', lYear: 1947, dYear: 'Ongoing' },
        { id: 32, name: 'KCAL-TV', country: 'United States of America', lYear: 1948, dYear: 'Ongoing' },
        { id: 33, name: 'KCBS-TV', country: 'United States of America', lYear: 1948, dYear: 'Ongoing' },
        { id: 34, name: 'KCOP-TV', country: 'United States of America', lYear: 1948, dYear: 'Ongoing' },
        { id: 35, name: 'KING-TV', country: 'United States of America', lYear: 1948, dYear: 'Ongoing' },
        { id: 36, name: 'KOB', country: 'United States of America', lYear: 1948, dYear: 'Ongoing' },
        { id: 37, name: 'KPIX-TV', country: 'United States of America', lYear: 1948, dYear: 'Ongoing' },
        { id: 38, name: 'KSTP-TV', country: 'United States of America', lYear: 1948, dYear: 'Ongoing' },
        { id: 39, name: 'KTVX', country: 'United States of America', lYear: 1948, dYear: 'Ongoing' },
        { id: 40, name: 'KXAS-TV', country: 'United States of America', lYear: 1948, dYear: 'Ongoing' },
        { id: 41, name: 'Paramount Television Network', country: 'United States of America', lYear: 1948, dYear: 1956 },
        { id: 42, name: 'WABC-TV', country: 'United States of America', lYear: 1948, dYear: 'Ongoing' },
        { id: 43, name: 'WAVE', country: 'United States of America', lYear: 1948, dYear: 'Ongoing' },
        { id: 44, name: 'WBAL-TV', country: 'United States of America', lYear: 1948, dYear: 'Ongoing' },
        { id: 45, name: 'WBZ-TV', country: 'United States of America', lYear: 1948, dYear: 'Ongoing' },
        { id: 46, name: 'WCAU', country: 'United States of America', lYear: 1948, dYear: 'Ongoing' },
        { id: 47, name: 'WDSU', country: 'United States of America', lYear: 1948, dYear: 'Ongoing' },
        { id: 48, name: 'WGN-TV', country: 'United States of America', lYear: 1948, dYear: 'Ongoing' },
        { id: 49, name: 'WIVB-TV', country: 'United States of America', lYear: 1948, dYear: 'Ongoing' },
        { id: 50, name: 'WJBK', country: 'United States of America', lYear: 1948, dYear: 'Ongoing' },
        { id: 51, name: 'WJZ-TV', country: 'United States of America', lYear: 1948, dYear: 'Ongoing' },
        { id: 53, name: 'WKYC', country: 'United States of America', lYear: 1948, dYear: 'Ongoing' },
        { id: 54, name: 'WLS-TV', country: 'United States of America', lYear: 1948, dYear: 'Ongoing' },
        { id: 55, name: 'WLWT', country: 'United States of America', lYear: 1948, dYear: 'Ongoing' },
        { id: 56, name: 'WMAQ-TV', country: 'United States of America', lYear: 1948, dYear: 'Ongoing' },
        { id: 57, name: 'WMC-TV', country: 'United States of America', lYear: 1948, dYear: 'Ongoing' },
        { id: 58, name: 'WNAC-TV', country: 'United States of America', lYear: 1948, dYear: 1982 },
        { id: 59, name: 'WNET', country: 'United States of America', lYear: 1948, dYear: 'Ongoing' },
        { id: 60, name: 'WPIX', country: 'United States of America', lYear: 1948, dYear: 'Ongoing' },
        { id: 61, name: 'WSB-TV', country: 'United States of America', lYear: 1948, dYear: 'Ongoing' },
        { id: 62, name: 'WTNH', country: 'United States of America', lYear: 1948, dYear: 'Ongoing' },
        { id: 63, name: 'WTVG', country: 'United States of America', lYear: 1948, dYear: 'Ongoing' },
        { id: 64, name: 'WTVH', country: 'United States of America', lYear: 1948, dYear: 'Ongoing' },
        { id: 65, name: 'WTVR-TV', country: 'United States of America', lYear: 1948, dYear: 'Ongoing' },
        { id: 66, name: 'WXYZ-TV', country: 'United States of America', lYear: 1948, dYear: 'Ongoing' }
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
