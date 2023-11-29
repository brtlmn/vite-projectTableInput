<script setup>
import HelloWorld from './components/HelloWorld.vue'

import csv from './assets/Table_Input.csv'
console.log(csv) 

var A5 = csv.filter(function(row){
  return row ['Index #'] == 'A5';
})[0]['Value']; 
console.log(A5); 

var A20 = csv.filter(function(row){
  return row ['Index #'] == 'A20';
})[0]['Value']; 
console.log(A20); 

var A15 = csv.filter(function(row){
  return row ['Index #'] == 'A15';
})[0]['Value']; 
console.log(A15); 

var A7 = csv.filter(function(row){
  return row ['Index #'] == 'A7';
})[0]['Value']; 
console.log(A7); 

var A13 = csv.filter(function(row){
  return row ['Index #'] == 'A13';
})[0]['Value']; 
console.log(A13); 

var A12 = csv.filter(function(row){
  return row ['Index #'] == 'A12';
})[0]['Value']; 
console.log(A12); 

var Alpha = parseInt(A5) + parseInt(A20)
var Beta = parseInt(A15)/parseInt(A7) 
var Charlie = parseInt(A13)*parseInt(A12)

</script>

<template>
  <div>
    <a href="https://vitejs.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
  </div>
  <HelloWorld msg="Hanis Syafiqa Khairil Azli" />

  <table>
  <tr>
    <th>Index #</th>
    <th>Value</th> 
  </tr>
  <tr v-for="row in csv" :key="row['Index #']">
        <td>{{row['Index #']}}</td>
        <td>{{row['Value']}}</td>
      </tr>
</table>

<table>
  <tr>
    <th>Category</th>
    <th>Value</th>
  </tr>
  <tr>
    <td>Alpha</td>
    <td>{{ Alpha }}</td>
  </tr>
  <tr>
    <td>Beta</td>
    <td>{{ Beta }}</td>
  </tr>
  <tr>
    <td>Charlie</td>
    <td>{{ Charlie }}</td>
  </tr>


</table>

</template>




<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
