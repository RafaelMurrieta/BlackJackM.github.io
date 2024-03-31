<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <mytable/>

</template>

<script>
import mytable from './components/table.vue';

export default {
  name: 'App',
  components: {
   mytable,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center; 
  margin-top: 0;
  padding: 0;
}
</style>

