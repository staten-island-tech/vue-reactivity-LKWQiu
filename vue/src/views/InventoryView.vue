<template>
  <div class="Inventory"> 
<!--     <h3 v-if="data.Rolls > 10000"> U HAVE REACHED MAX ROLLS</h3>
    <h3 v-else> You have rolled {{data.Rolls}} times</h3> -->
    <button v-on:click="RandomNumber()"> ROLL </button>
<!--     <p v-if="data.Mercuryamount > 0"> U got {{ data.Mercuryamount }} Mercury</p>
    <br>
    <p v-if="data.Marsamount > 0"> U got {{ data.Marsamount }} Mars</p>
    <br>
    <p v-if="data.Uranusamount > 0"> U got {{ data.Uranusamount }} Uranus</p>
    <br>
    <p v-if="data.Venusamount > 0"> U got {{ data.Venusamount }} Venus</p>
    <br>
    <p v-if="data.Jupiteramount > 0"> U got {{ data.Jupiteramount }} Jupiter</p>
    <br>
    <p v-if="data.Neptuneamount > 0"> U got {{ data.Neptuneamount }} Neptune</p>
    <br>
    <p v-if="data.Earthamount > 0"> U got {{ data.Earthamount }} Earth</p>
    <br>
    <p v-if="data.Saturnamount > 0"> U got {{ data.Saturnamount }} Saturn</p>
    <br>
    <p v-if="data.Plutoamount > 0"> U got {{ data.Plutoamount }} Pluto</p>
    <br>
    <p v-if="data.Sunamount > 0"> U got {{ data.Sunamount }} Sun</p> -->
  </div>

  <div class="History1" 
  style="  
  max-height: 70vh;
  max-width: 15vh;
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  position: absolute;
  right: 20%;
  margin-top: 5%;
  overflow-y: scroll;" >
  </div>
  
  <div class="DestCard1">
    <DestCard
    v-for="randomNum in Destination"
    :key="Destination.name"
    :Destination="randomNum"
    />
  </div>

</template>


<script setup>
  import DestCard from '@/components/DestCard.vue';
  var data = {
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
    };


    function RollMercury(){
      console.log("works?");
        data.Mercuryamount++;
        const carder = `
        <p> You rolled a Mercury</p>
        `
        document.querySelector(".History1").insertAdjacentHTML("beforeend", carder)
    };
    function RollMars(){
      console.log("works?");
        data.Marsamount++;
        const carder = `
        <p> You rolled a Mars</p>
        `
        document.querySelector(".History1").insertAdjacentHTML("beforeend", carder)
    };
    function RollUranus(){
      console.log("works?");
        data.Uranusamount++;
        const carder = `
        <p> You rolled a Uranus</p>
        `
        document.querySelector(".History1").insertAdjacentHTML("beforeend", carder)
    };
    function RollVenus(){
      console.log("works?");
        data.Venusamount++;
        console.log(data.Venusamount);
        const carder = `
        <p> You rolled a Venus</p>
        `
        document.querySelector(".History1").insertAdjacentHTML("beforeend", carder)
    };
    function RollJupiter(){
      console.log("works?");
        data.Jupiteramount++
        const carder = `
        <p> You rolled a Jupiter</p>
        `
        document.querySelector(".History1").insertAdjacentHTML("beforeend", carder)
    };
    function RollNeptune(){
      console.log("works?");
        data.Neptuneamount++;
        const carder = `
        <p> You rolled a Neptune</p>
        `
        document.querySelector(".History1").insertAdjacentHTML("beforeend", carder)
    };
    function RollEarth(){
      console.log("works?");
        data.Earthamount++;
        const carder = `
        <p> You rolled a Earth</p>
        `
        document.querySelector(".History1").insertAdjacentHTML("beforeend", carder)
    };
    function RollSaturn(){
      console.log("works?");
        data.Saturnamount++;
        const carder = `
        <p> You rolled a Saturn</p>
        `
        document.querySelector(".History1").insertAdjacentHTML("beforeend", carder)
    };
    function RollPluto(){
      console.log("works?");
        data.Plutoamount++;
        const carder = `
        <p> You rolled a Pluto</p>
        `
        document.querySelector(".History1").insertAdjacentHTML("beforeend", carder)
    };
    function RollSun(){
      console.log("works?");
        data.Sunamount++;
        const carder = `
        <p> You rolled a Sun</p>
        `
        document.querySelector(".History1").insertAdjacentHTML("beforeend", carder)
    };

    function RandomNumber() {
      const myNums = ['Mercury', 'Mars', 'Uranus', 'Venus', 'Jupiter', 'Neptune', 'Earth', 'Saturn', 'Pluto', 'Sun'];
      const randomNum = myNums[Math.floor(Math.random() * myNums.length)];
      data.randomNum = randomNum;
      data.Rolls++
      if(randomNum === 'Mercury'){
        RollMercury();
        const randomNum = [
        {
          name: "Venetian Renaissance",
          International: true,
          price: 1300,
          img: "https://images.unsplash.com/photo-1498307833015-e7b400441eb8?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1528&q=80&quot;",
        },
      ];
      }
      if(randomNum === 'Mars'){
        RollMars();
      }
      if(randomNum === 'Uranus'){
        RollUranus();
      }
      if(randomNum === 'Venus'){
        RollVenus();
      }
      if(randomNum === 'Jupiter'){
        RollJupiter();
      }
      if(randomNum === 'Neptune'){
        RollNeptune();
      }
      if(randomNum === 'Earth'){
        RollEarth();
      }
      if(randomNum === 'Saturn'){
        RollSaturn();
      }
      if(randomNum === 'Pluto'){
        RollPluto();
      }
      if(randomNum === 'Sun'){
        RollSun();
      }
      else()=>{
        console.log("U a Bafoon")
      }
      console.log(randomNum)
    };



</script>


<style scoped>
.Inventory {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding-top: 30%;
  };

.Inventory button{
  padding: 20px;
  background-color: black;
  color: white;
};

.DestCard1{
  max-width: 40%;
  height: 50%;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-top: 30%;
  position: absolute;
  right: 0;
};

.DestCard1 img{
  object-fit: contain;
};
</style>
