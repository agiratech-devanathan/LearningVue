// UI Template 
<template>
<!-- binding text into html template using double curly brackets -->
<div>{{greet}} {{name}}</div>
<!-- Another way of binding the text -->
<div v-text="channel"></div>
</template>
//Logic template
<script>

export default {
  name: 'App',
 data(){
return{
  greet:'Hello',
  name:'Devas',
  channel:'Dj Code'
}
 }
}
</script>
// Style Template
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
