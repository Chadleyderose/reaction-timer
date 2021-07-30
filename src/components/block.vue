<template>
  <div class="block" v-if="showBlock">Click Me</div>
</template>

<script>
export default {
    prop:['Delay'],
    data(){
        return{
            showBlock:false
        }
    },
    mounted(){
        console.log('component mounted')
        setTimeout(() => {
            this.showBlock = true 
            console.log(this.Delay)
        }, this.Delay)
    },
    updated(){

    }
}
</script>

<style>
.block{
    width: 400px;
    border-radius: 20px;
    background: #0faf87;
    color: white;
    text-align: center;
    padding: 100px 0;
    margin: 40px auto;
}
</style>