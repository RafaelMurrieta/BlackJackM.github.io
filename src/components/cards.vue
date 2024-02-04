<template>
    <div class="my-card">
        <h1>{{message}}</h1>
        <span v-for="(number,index) in receivedList" :key="index">{{number}}</span>
        <!-- <span>numero: {{nm}}</span> -->
    </div>
</template>


<script>
export default {
    name: 'MyCard',
    data(){
        return{
            message: `Mi valor es`
        }
    },
    methods:{
        getcard(){
            console.log('valor');
        }
    },
    props:{
        receivedList:Array
    }
}
</script>