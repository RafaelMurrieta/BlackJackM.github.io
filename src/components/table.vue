<template>
    <div class="my-table">   
        <div class="bank">
            <div class="cards-back">
                
            </div>
            <div class="gamerCard">

            </div>
            <div class="money">

            </div>
        </div>
        <div class="player">
            <div class="buttons">
                <button v-on:click="randomNumber">{{message}}</button>
            </div>
            <div class="cards">

            </div>
            <div class="numbers-container"> <!-- Nuevo contenedor para los números -->
                <div class="numbers" v-bind:style="{ overflow: list.length > 5 ? 'auto' : 'visible' }"> <!-- Aplicando overflow según la longitud de la lista -->
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
let rest = 0
export default {
    name: 'MyTable',
    data(){
        return{
            message: 'HIT',
            list:[  
                
            ]
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
    background: black;
}
.bank > div{
    width: auto;
    background: red;
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
