<template>
<h1>Speedy Reaction Timer</h1>
<button @click="start" :disabled="isPlaying">Play</button>
<Block v-if="isPlaying" :delay="Delay"/>
</template>

<script>
import Block from './components/Block'
export default {
  name: 'App',
  components: {Block},
  data(){
    return{
      isPlaying: false,
      Delay:null
    }
  },
  methods:{
    start(){
      this.Delay = 2000 + Math.random() * 5000
      this.isPlaying = true
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #444;
  margin-top: 60px;
}
</style>
