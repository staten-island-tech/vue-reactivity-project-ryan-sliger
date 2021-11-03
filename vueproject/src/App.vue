<template>
  <div id= "app">
    <h1 class="main">
      Welcome To T-Shirt Customizer
    </h1>
    <div class="button-container">
      <p>Pick a Logo</p>
    </div>

    <div class="btn" v-for="logo in logos" v-bind:key="logo.name">
      <button v-on:click="updateLogo(logo.logoImageL)">{{ logo.name }}</button>
    </div>


    <div class="image_cont">
      <img :src="image" class="shirt" >
      <img :src="imageL" class="logo">
    </div>
  
  </div>
    
  
</template>

<script>

export default {
  name: 'App',

  data() {

    return {
      image: require("./assets/blank-tshirt.jpg"),
      imageL: require("./assets/Logo.png"),
      logos: [{
        name: "nike",
        logoImageL: require("./assets/nike.png")
      },{
        name: "under armor",
        logoImageL: require("./assets/under-armor.png"),
      },{
        name: "supreeme",
        logoImageL: require("./assets/supreeme.png"),
      }]
};
  },methods:{
  updateLogo(logoImageL) {
    this.imageL = logoImageL
  }}
};


</script>

<style>


#app {
  font-family: Comic Sans MS;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: brown;
}

.btn{
  padding: 1rem;
  display: flex;
  flex-direction: row;
}

.UA{
  margin: 2rem;
}
.shirt{
  z-index: 2;
  position: absolute;
  margin: auto;
  left: 37.5%;
  top: 20%;

}
.logo{
  height: 8rem;
  width: 8rem;
  z-index: 3;
  position: absolute;
  left: 45%;
  top: 35%;
}


</style>
