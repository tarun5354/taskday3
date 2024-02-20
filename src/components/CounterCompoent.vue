<template>
    <div class="items1">
        <h1> The bug counter</h1>
        <button @click.prevent="decreaseCounter()">-</button>
        <span>
            {{ counter }}
        </span>
        <button @click.prevent="IncreaseCounter()">+</button>
    </div>

</template>
<script setup>
import { ref } from 'vue'
const counter=ref(0);

function IncreaseCounter(){
    counter.value++;

}
function decreaseCounter(){
    counter.value--;

}
</script>
<style scoped>
.items1{
    text-align: center;
}
button{display:inline-block;
    width:50px ;
    height: 40px;
    background-color: rgb(205, 212, 212);
    border-radius: 10px;
    margin:30px 30px;
    padding: 2px;
    gap: 10;
}

</style>