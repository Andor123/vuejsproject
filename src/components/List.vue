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
        { id: 66, name: 'WXYZ-TV', country: 'United States of America', lYear: 1948, dYear: 'Ongoing' },
        { id: 67, name: 'Bayerischer Rundfunk', country: 'Germany', lYear: 1949, dYear: 'Ongoing' },
        { id: 68, name: 'BBC West Midlands', country: 'United Kingdom', lYear: 1949, dYear: 'Ongoing' },
        { id: 69, name: 'KABC-TV', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 70, name: 'KC2XAK', country: 'United States of America', lYear: 1949, dYear: 1952 },
        { id: 71, name: 'KDFW', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 72, name: 'KDKA-TV', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 73, name: 'KFMB-TV', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 74, name: 'KFOR-TV', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 75, name: 'KGO-TV', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 76, name: 'KMTV-TV', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 77, name: 'KNBC', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 78, name: 'KOTV-DT', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 79, name: 'KPHO-TV', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 80, name: 'KPRC-TV', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 81, name: 'KRON-TV', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 82, name: 'KSL-TV', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 83, name: 'KTTV', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 84, name: 'KWQC-TV', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 85, name: 'Radiodiffusion-Télévision Française', country: 'France', lYear: 1949, dYear: 1964 },
        { id: 86, name: 'WAGA-TV', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 87, name: 'WBNG-TV', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 88, name: 'WBNS-TV', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 89, name: 'WBRC', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 90, name: 'WBTV', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 91, name: 'WCCO-TV', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 92, name: 'WCMH-TV', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 93, name: 'WCPO-TV', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 94, name: 'WDAF-TV', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 95, name: 'WDTN', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 96, name: 'WFAA', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 96, name: 'WFMY-TV', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 97, name: 'WGAL', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 98, name: 'WHIO-TV', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 99, name: 'WICU-TV', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 100, name: 'WJAC-TV', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 101, name: 'WJAR', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 102, name: 'WJW', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 103, name: 'WJXT', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 104, name: 'WKRC-TV', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 105, name: 'WKTV', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 106, name: 'WOAI-TV', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 107, name: 'WOOD-TV', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 108, name: 'WOWT', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 109, name: 'WROC-TV', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 110, name: 'WRTV', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 111, name: 'WSAZ-TV', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 112, name: 'WSYX', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 113, name: 'WTTV', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 114, name: 'WTVJ', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 115, name: 'WUSA', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 116, name: 'WVTM-TV', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 117, name: 'WVUE', country: 'United States of America', lYear: 1949, dYear: 1958 },
        { id: 118, name: 'WWOR-TV', country: 'United States of America', lYear: 1949, dYear: 'Ongoing' },
        { id: 119, name: 'CMQ', country: 'Cuba', lYear: 1950, dYear: 1959 },
        { id: 120, name: 'Cuban Institute of Radio and Television', country: 'Cuba', lYear: 1950, dYear: 'Ongoing' },
        { id: 121, name: 'Cubavisión', country: 'Cuba', lYear: 1950, dYear: 'Ongoing' },
        { id: 122, name: 'France 3 Nord-Pas-de-Calais', country: 'France', lYear: 1950, dYear: 'Ongoing' },
        { id: 123, name: 'France 3 Picardie', country: 'France', lYear: 1950, dYear: 'Ongoing' },
        { id: 124, name: 'KENS', country: 'United States of America', lYear: 1950, dYear: 'Ongoing' },
        { id: 125, name: 'Rede Tupi', country: 'Brazil', lYear: 1950, dYear: 1980 },
        { id: 126, name: 'WHAS-TV', country: 'United States of America', lYear: 1950, dYear: 'Ongoing' },
        { id: 127, name: 'WHBF-TV', country: 'United States of America', lYear: 1950, dYear: 'Ongoing' },
        { id: 128, name: 'WLNS-TV', country: 'United States of America', lYear: 1950, dYear: 'Ongoing' },
        { id: 129, name: 'WOI-DT', country: 'United States of America', lYear: 1950, dYear: 'Ongoing' },
        { id: 130, name: 'WSMV-TV', country: 'United States of America', lYear: 1950, dYear: 'Ongoing' },
        { id: 131, name: 'WSTM-TV', country: 'United States of America', lYear: 1950, dYear: 'Ongoing' },
        { id: 132, name: 'WTKR', country: 'United States of America', lYear: 1950, dYear: 'Ongoing' },
        { id: 133, name: 'WWMT', country: 'United States of America', lYear: 1950, dYear: 'Ongoing' },
        { id: 134, name: 'XHTV-TDT', country: 'Mexico', lYear: 1950, dYear: 'Ongoing' },
        { id: 135, name: 'BBC North', country: 'United Kingdom', lYear: 1951, dYear: 'Ongoing' },
        { id: 136, name: 'Canal 5', country: 'Mexico', lYear: 1951, dYear: 'Ongoing' },
        { id: 137, name: 'Channel One Russia', country: 'Russia', lYear: 1951, dYear: 'Ongoing' },
        { id: 138, name: 'DR', country: 'Denmark', lYear: 1951, dYear: 'Ongoing' },
        { id: 139, name: 'DR1', country: 'Denmark', lYear: 1951, dYear: 'Ongoing' },
        { id: 140, name: 'Dutch Public Broadcasting System', country: 'Netherlands', lYear: 1951, dYear: 'Ongoing' },
        { id: 141, name: 'Las Estrellas', country: 'Mexico', lYear: 1951, dYear: 'Ongoing' },
        { id: 142, name: 'NPO 1', country: 'Netherlands', lYear: 1951, dYear: 'Ongoing' },
        { id: 143, name: 'Tanzania Broadcasting Corporation', country: 'Tanzania', lYear: 1951, dYear: 'Ongoing' },
        { id: 144, name: 'Theater Television Network', country: 'United States of America', lYear: 1951, dYear: 1953 },
        { id: 145, name: 'Televisión Pública Argentina', country: 'Argentina', lYear: 1951, dYear: 'Ongoing' },
        { id: 146, name: 'WXIA-TV', country: 'United States of America', lYear: 1951, dYear: 'Ongoing' },
        { id: 147, name: 'XELD-TV', country: 'Mexico', lYear: 1951, dYear: 1954 },
        { id: 148, name: 'XEPM-TDT', country: 'Mexico', lYear: 1951, dYear: 'Ongoing' },
        { id: 149, name: 'XEW-TDT', country: 'Mexico', lYear: 1951, dYear: 'Ongoing' }
      ],
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
