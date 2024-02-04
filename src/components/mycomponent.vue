<template>
    <div class="my-component">
        <h1 v-if="IsVisible">{{ message }}</h1>
        <h1 v-bind:class="{  HighLighted: isHighLighted }">{{ title }}</h1>
        <button v-on:click="ToggleHighlight" >Toggle HighLight</button>
        <button v-on:click="sayHello" >Toogle visibility</button>
        <input v-model="message">
        <ul>
            <li v-for="item in list" :key="item.id">{{ item.text }}</li>
        </ul>
    </div>
</template>

<style>
.HighLighted{
    color: yellow;
}
</style>

<script>
export default{
    name: 'MyComponent',
    data(){
        return{
            message: 'Hello world Vue',
            IsVisible:true,
            title: 'This is the tittle',
            isHighLighted:false,
            list:[
                {id: 1, text: 'first'},
                {id: 2, text: 'two'},
                {id: 3, text: 'three'}
            ]
        }
    },
    methods:{
        ToggleVisibility(){
            this.IsVisible = !this.IsVisible;
        },
        sayHello(){
            alert('Holaa')
        },
        ToggleHighlight(){
            this.isHighLighted = !this.isHighLighted;
        },
}

}

</script>