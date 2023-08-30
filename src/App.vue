// UI Template 
<template>
<!-- binding text into html template using double curly brackets -->
<div>{{greet}} {{name}}</div>
<!-- Another way of binding the text -->
<!-- it wont't work foe html binding -->
<div v-text="channel"></div> 
<!-- Binding HTML content into Html template using V-html attributes -->
<div v-html="channel"></div>
<div v-html="hack"></div>
</template>
//Logic template
<script>

export default {
  name: 'App',
 data(){
return{
  greet:'Hello',
  name:'Devas',
  channel:'<b>Dj Code</b>',
  hack:`<a href="#' onclick="alert('you have been hacked')">Win a prize</a>`,
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
