<template>
    <div class="my-table">   
        <div class="bank">
            <div class="cards-back">
                <div>
                    <span></span>
                </div>
            </div>
            <div class="gamerCard">

            </div>
            <div class="money">
                <mony-area></mony-area>
            </div>
        </div>
        <div class="player">
            <div class="buttons">
                <button v-on:click="randomNumber">{{message}}</button>
            </div>
            <div class="cards">
                <my-card></my-card>
            </div>
            <div class="numbers-container"> 
                <div class="numbers" v-bind:style="{ overflow: list.length > 5 ? 'auto' : 'visible' }"> 
                    <h1>
                        <span v-for="(number, index) in list" :key="index">
                            {{ number }}{{ index < list.length - 1 ? ', ' : '' }}
                        </span>
                    </h1>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import monyArea from './monyArea.vue';
import myCard from './cards.vue'


let rest = 0
export default {
  components: { monyArea, myCard },
    name: 'MyTable',
    data(){
        return{
            message: 'HIT',
            list:[]
        }
    },
    methods:{
        randomNumber() {
            let nm = Math.floor(Math.random() * 13)
            rest+=nm;   
            if (rest<21) {
                this.list.push(nm)                    
            }else{
                this.list.push(nm)                    
                alert("Perdiste")
            }
        }
    },
};
</script>

<style>
.my-table{
    display: grid;
    width: 90vw;
    height: 90vh;
    border: 1rem solid #502E1D;
    background-color: rgb(36, 155, 36);
}
.bank{
    display: flex;
    width: 100%;
    margin: 0 5% 0 5%;
}
.bank > div{
    display: grid;
    width: 30%;
    border: 1px solid black;
}
.bank .cards-back{
    justify-content: center;
    align-items: center;
}
.bank .cards-back div{
    border-radius: 10px;
    display: grid;
    justify-content: center;
    align-content: center;
    background: black;
    height: 10%;
    width: 15vw;
    border: 1px solid black;
}
.bank .cards-back div span{
    display: grid;
    border-radius: 10px;
    background: gray;
    width: 10vw;
    height: 5px;
}
.player{
    display: grid;
    width: 100%;
}

.player .numbers-container {
    position: relative;
    justify-content: center;
    display: flex;
    max-width: 80%;
}

.player .numbers h1{
    width: 100%;
    display: flex;
}

</style>
