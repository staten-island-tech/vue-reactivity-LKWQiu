<template>
  <div class="Inventory">

    <button v-on:click="RandomNumber()"> ROLL </button>
    <p v-if="randomNum > 1"> STARR</p>
    <p v-else> U suck</p>

<!--     <p v-if="amount > 0">
      You have {{ amount }} stars
    </p>

    <p v-else>
      U have nothing in your inventory.
      <br>
      Use the gatcha.
    </p>

    <button v-on:click="RollGatch()">
      Roll
    </button> -->
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .Inventory {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>

<script>
export default{
  data() {
     return {
    } 
  },
  methods: {
    /* RollGatch(){
      this.amount++;
      alert('U rolled something!!!')
    } */

    RandomNumber(){
      const myNums = ['1', '2', '3', '4', '5', '6', '7', '8', '9', '0'];  
      const randomNum = myNums[Math.floor(Math.random() * myNums.length)];  
      console.log(randomNum)
    }
  },
}

</script>
