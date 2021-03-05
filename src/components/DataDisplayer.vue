<template>
  <div class="dataDispayer">
    <table>
    <tbody>
    <tr>
    <td colspan="2"> <h2 class="dataDispayer-header" v-if="Header">{{ Header }}</h2></td>
    </tr>
    <div v-for="data in datas" v-bind:key="data">
    <tr>
    <td class="key"><b>{{ data.key }}</b> </td>
    <td class="value">{{ data.value }}</td>
    </tr>
    </div>
    </tbody>
    </table>
  </div>
</template>

<script>

export default {
  props: [
    'Header',
    'datas'
  ]
}
</script>

<style>
table {
font-family: arial, sans-serif;
border-collapse: collapse;
width: 100%;
}

td, th {
border: 0px solid #dddddd;
text-align:left;
padding: 10px;

}

.key {
  width: 250px;
}
.value {
  text-align:right;
  width: 60px;
}

tr:nth-child(even) {
background-color: #dddddd;
}
</style>