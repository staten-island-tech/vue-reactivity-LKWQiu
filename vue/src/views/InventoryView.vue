<template>
  <div class="Inventory"> 

    <h3 v-if="Rolls > 10000"> U HAVE REACHED MAX ROLLS</h3>
    <h3 v-else> You have Rolled {{Rolls}} times</h3>
    <button v-on:click="RandomNumber()"> ROLL </button>
    <p v-if="Mercuryamount > 0"> U got {{ Mercuryamount }} Mercury</p>
    <br>
    <p v-if="Marsamount > 0"> U got {{ Marsamount }} Mars</p>
    <br>
    <p v-if="Uranusamount > 0"> U got {{ Uranusamount }} Uranus</p>
    <br>
    <p v-if="Venusamount > 0"> U got {{ Venusamount }} Venus</p>
    <br>
    <p v-if="Jupiteramount > 0"> U got {{ Jupiteramount }} Jupiter</p>
    <br>
    <p v-if="Neptuneamount > 0"> U got {{ Neptuneamount }} Neptune</p>
    <br>
    <p v-if="Earthamount > 0"> U got {{ Earthamount }} Earth</p>
    <br>
    <p v-if="Saturnamount > 0"> U got {{ Saturnamount }} Saturn</p>
    <br>
    <p v-if="Plutoamount > 0"> U got {{ Plutoamount }} Pluto</p>
    <br>
    <p v-if="Sunamount > 0"> U got {{ Sunamount }} Sun</p>

  </div>
</template>

<style>
@media (min-width: 1024px) {
  .Inventory {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding-top: 30%;
  }
}
</style>

<script>
export default{
   data() {
      return {
        Rolls: 0,
        randomNum: '',
        Mercuryamount : 0,
        Marsamount : 0,
        Uranusamount: 0,
        Venusamount: 0,
        Jupiteramount: 0,
        Neptuneamount: 0,
        Earthamount: 0,
        Saturnamount: 0,
        Plutoamount: 0,
        Sunamount: 0,
     } 
   },
  methods: {

     RollMercury(){
      console.log("works?");
        this.Mercuryamount++;
    },
    RollMars(){
      console.log("works?");
        this.Marsamount++;
    },
    RollUranus(){
      console.log("works?");
        this.Uranusamount++;
    },
    RollVenus(){
      console.log("works?");
        this.Venusamount++;
    },
    RollJupiter(){
      console.log("works?");
        this.Jupiteramount++
    },
    RollNeptune(){
      console.log("works?");
        this.Neptuneamount++;
    },
    RollEarth(){
      console.log("works?");
        this.Earthamount++;
    },
    RollSaturn(){
      console.log("works?");
        this.Saturnamount++;
    },
    RollPluto(){
      console.log("works?");
        this.Plutoamount++;
    },
    RollSun(){
      console.log("works?");
        this.Sunamount++;
    },

    RandomNumber() {
      const myNums = ['Mercury', 'Mars', 'Uranus', 'Venus', 'Jupiter', 'Neptune', 'Earth', 'Saturn', 'Pluto', 'Sun'];
      const randomNum = myNums[Math.floor(Math.random() * myNums.length)];
      this.randomNum = randomNum;
      this.Rolls++
      if(randomNum === 'Mercury'){
        this.RollMercury();
      }
      if(randomNum === 'Mars'){
        this.RollMars();
      }
      if(randomNum === 'Uranus'){
        this.RollUranus();
      }
      if(randomNum === 'Venus'){
        this.RollVenus();
      }
      if(randomNum === 'Jupiter'){
        this.RollJupiter();
      }
      if(randomNum === 'Neptune'){
        this.RollNeptune();
      }
      if(randomNum === 'Earth'){
        this.RollEarth();
      }
      if(randomNum === 'Saturn'){
        this.RollSaturn();
      }
      if(randomNum === 'Pluto'){
        this.RollPluto();
      }
      if(randomNum === 'Sun'){
        this.RollSun();
      }
      else()=>{
        console.log("U a Bafoon")
      }
      console.log(randomNum)
    },
  },
}

</script>
