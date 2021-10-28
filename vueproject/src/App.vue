<template>
  <div id= "app">
    <h1 class="main">
      Welcome To T-Shirt Customizer
    </h1>
    <div>
      <img v-bind:src="image">
    </div>
  
  </div>
    
  
</template>

<script>

export default {
  name: 'App',

  data() {
    return {
      logo: [{
        name: "nike",
        image: require(nike.png)
      },{
        name: "under armor",
        image: require(under_armor.png),
      },{
        name: "supreeme",
        image: require(supreeme.png),
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
  margin-top: 60px;
}
</style>
