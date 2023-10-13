<script setup>
// import Fruts  from './components/Fruts.vue'
import Active  from './components/V-on.vue'


const fruts=['🍓🍓🍒🍌🌽🥒🥬🥦🥔🍉🍈']
const canastFruts=[
  {
  nameFrut:'Mango',
  price:10.5,
  huert:'San Lois' 
},
{
  nameFrut:'Apple',
  price:50,
  huert:'San Anne' 
},
{
  nameFrut:'Berry',
  price:115,
  huert:'San Lois' 
},
{
  nameFrut:'Pinapple',
  price:10.0,
  huert:'George' 
},
]
const exampleObject={
  nameFrut:'Apple',
  price:50,
  huert:'San Anne'
}

</script>

<template>
 <div id="app">
  <h2 class="p-2 text-center mb-3">{{ fruts }}</h2>
  <!-- <Fruts :canastFruts="canastFruts" :exampleObject="exampleObject"/> -->
  <Active/>
 </div>
</template>

<style scoped>

</style>
