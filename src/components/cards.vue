<template>
    <div class="my-card">
        <h1>{{message}}</h1>
        <span v-for="(number,index) in receivedList" :key="index">{{number}}</span>
    </div>
</template>


<script>
export default {
    name: 'MyCard',
    message: 'hola',
    props:{
        receivedList:Array,
    }
}
</script>