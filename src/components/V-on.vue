<script setup>
import { computed, ref } from "vue"
// Variable reactiva
const displayActive = ref(0)
const listNum = ref([])


const addNumber = () =>
    displayActive.value++
const restNumber = () =>
    displayActive.value--
const ResetNumber = () => {
    displayActive.value = 0
    listNum.value.filter()
}
const addList = () => {
    const add = listNum.value.unshift(displayActive.value)
}
const comparationNumber = computed(() => {
    const number = listNum.value.find(num => num === displayActive.value)
       return number===0||number
})

</script>
<template>
    <div class="container text-center">
        <b v-if="displayActive > -1" :class="{ 'text-success': displayActive, 'text-danger': !displayActive }">
            {{ displayActive }}
        </b>
        <br>
        <button class="btn btn-primary m-2" @click="addNumber()">Aumentar</button>
        <button class="btn btn-secondary m-2" @click="ResetNumber()">Reset</button>
        <button class="btn btn-danger m-2" @click="restNumber()" :disabled="!displayActive">Disminuir</button>
        <button class="btn btn-success m-2" @click="addList()" :disabled="comparationNumber">Add</button>
        <br>
        <ul class="navbar-nav">
            <li class="nav-item" v-for="(item, index) in listNum" :key="index">
                {{ item }}
            </li>
        </ul>
    </div>
</template>
