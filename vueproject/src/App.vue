<template>
  <div id= "app">
    <h1 class="main">
      Welcome To T-Shirt Customizer
    </h1>
    <div class="button-container">
      <button class="nike" alt="btn">Nike</button>
      <button class="UA" alt="btn">under_armor</button>
      <button class="Supreeme" alt="btn">Supreeme</button>
    </div>
    <div>
      <img :src="image">
    </div>
    <div>
      <h2 class="logo-name">{{name}}</h2>
    </div>
  
  </div>
    
  
</template>

<script>

export default {
  name: 'App',

  data() {

    return {
      image: require("./assets/blank-tshirt.jpg"),
      logo: [{
        name: "nike",
        image: require("./assets/nike.png")
      },{
        name: "under armor",
        image: require("./assets/under-armor.png"),
      },{
        name: "supreeme",
        image: require("./assets/supreeme.png"),
      }]
};
  },
};
</script>

<style>


#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #502c2c;
  margin-top: 30px;
}

.button-container{
  padding: 1rem;
}

.UA{
  margin: 2rem;
}
</style>
