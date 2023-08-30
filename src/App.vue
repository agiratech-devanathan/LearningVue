// UI Template 
<template>

<h1 v-bind:id="headingId">Heading</h1>

<!-- binding true or false attributes -->
<button v-bind:disabled="isDisabled">Bind</button>
<!-- binding Class attribute -->
<h3 class=underline>UnderLine Text</h3>

<h2 class="underline" v-bind:class="status">Status</h2>

<h2 v-bind:class="isPromoted && 'promoted'">Promoted Movie</h2>

<h2 v-bind:class="isSoldOut ? 'sold-out':'new'">SoldOut Movie</h2>

<h2 v-bind:class="['new','promoted']">New promoted Movie </h2>

<h1 v-bind:class="[isPromoted && 'promoted',isSoldOut ? 'sold-out':'new']">Array Class conditionally</h1>

<h1 v-bind:class="{
  promoted:isPromoted,new:!isSoldOut,'sold-out':isSoldOut
}">Object conditionally Movie</h1>

<h2 v-bind:style="{
  color:highlighter,
  'font-size':headerSize+'px',
  padding:'20px'
}">Inline style</h2>

<h2 v-bind:style='headerStyleObject'>Style Object</h2>

<div v-bind:style="[baseStyleObject,successStyleObject]">Success Style</div>

</template>
//Logic template
<script>

export default {
  name: 'App',
 data(){
return{
  status:'success',
  headingId:'heading',
  isDisabled:true,
  isPromoted:true,
  isSoldOut:true,
  highlighter:"orange",
  headerSize:80,
  headerStyleObject:{
    color:"purple",
    'font-size':"100px",
    padding:'20px'
  },
  baseStyleObject:{
    fontSize:"40px",
    padding:"10px"
  },

  successStyleObject:{
    color:'green',
    backgroundColor:'yellow',
    border:'2px solid green'
  }
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

.underline{
  text-decoration: underline  ;
}

.promoted{
  font-style: italic;
}

.new{
  color: greenyellow;
}

.sold-out{
color: red;
}
</style>
