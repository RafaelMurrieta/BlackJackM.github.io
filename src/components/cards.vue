<template>
    <div class="my-card">
        <h1>{{message}}</h1>
        <span v-for="(number,index) in receivedList" :key="index">{{number}}</span>
    </div>
</template>


<script>
import cardsInfo from '../consts/cards.ts';
var card = cardsInfo


export default {
    name: 'MyCard',
    info: card,
    message: 'hola',
    props:{
        receivedList:Array,
    }
}
</script>