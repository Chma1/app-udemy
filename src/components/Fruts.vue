<script setup>
defineProps({
  canastFruts: Array,
  exampleObject: Object
})
</script>

<template>
  <div class="container">
    <div class="row">
      <div class="col-sm-6">
        <h4 class="text-center display-3">Object</h4>

        <div class="card mb-2 text-center" v-for="(index,properity,value) in exampleObject" :key='index'>
          <span>{{ index }}--{{ properity }}--{{ value }}</span>
        </div>
      </div>
      <div class="col-sm-6  ">
        <h4 class="text-center display-3">Array</h4>
        <div class="card mb-3 p-2" v-for="(fruts, index) in canastFruts" :key="index">
          <span>Fruit: {{ fruts.nameFrut }}</span>
          <span>Price: ${{ fruts.price }}</span>
          <span>Origin: {{ fruts.huert }}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
