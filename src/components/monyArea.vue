<template>
    <div class="container-money">
        <div class="smallchange">
            <img src="../assets/images/moneyTwo.svg">
        </div>
        <div class="money">
            <h1 id="howMuch"></h1>
        </div>
    </div>
</template>

<style>
.container-money{
    display: grid;
}
.smallchange{
    display: flex;
    justify-content: right;
    height: 80%;
    align-items: start;
}
.smallchange > img{
    position:absolute;
    width: 7%;
}
.money{
    display: grid;
    text-align: center;
}
.money h1{
    margin-left: 10%;
    position: absolute;
    font-size: 2rem;
}
</style>

<script>
export default{
    name:'moneyArea'
}
</script>