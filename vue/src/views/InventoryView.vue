<template>
  <div class="Inventory">
    <p v-if="amount > 0">
      You have {{ amount }} stars
    </p>

    <p v-else>
      U have nothing in your inventory.
      <br>
      Use the gatcha.
    </p>

    <button v-on:click="RollGatch()">
      Roll
    </button>
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
      amount: 0,
    }
  },
  methods: {
    RollGatch(){
      this.amount++;
      alert('U rolled something!!!')
    }
  },
}

</script>
