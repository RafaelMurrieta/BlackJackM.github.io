<template>
    <div class="my-table">   
    <button v-on:click="randomNumber">{{message}}</button>
    <h1><span v-for="(number, index) in list" :key="index">
        {{ number }}{{ index < list.length - 1 ? ', ' : '' }}
      </span></h1>
      <mycard :receivedList="list"/>
    </div>
    
</template>


<script>
import mycard from './cards.vue'
export default {
    name: 'MyTable',
        data(){
            return{
                message: 'Preciona aqui',
                list:[  
                    1,2,3
                ]
            }
        },
        methods:{
            randomNumber() {
                let nm = Math.floor(Math.random() * 13)
                this.list.push(nm)
            }

        },
        components:{
            mycard
        }
};

</script>
