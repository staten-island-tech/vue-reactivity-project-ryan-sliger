<template>
  <div id= "app">
    <h1 class="main">
      Welcome To T-Shirt Customizer
    </h1>
    <div class="button-container">
      <button class="nike" alt="btn">Nike</button>
      <button class="UA" alt="btn">under_armor</button>
      <button class="Supreeme" alt="btn">Supreme</button>
    </div>
    <div class="image_cont">
      <img :src="image" class="shirt" >
      <img :src="imageL" class="logo">
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
      imageL: require("./assets/Logo.png"),
      logo: [{
        name: "nike",
        imageL: require("./assets/nike.png")
      },{
        name: "under armor",
        imageL: require("./assets/under-armor.png"),
      },{
        name: "supreeme",
        imageL: require("./assets/supreeme.png"),
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
}

.button-container{
  padding: 1rem;
}

.UA{
  margin: 2rem;
}
.shirt{
  z-index: 2;
  position: relative;
}
.logo{
  height: 8rem;
  width: 8rem;
  z-index: 3;
  position: relative;
}


</style>
