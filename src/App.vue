<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome ひめたんんんんんんん"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {
    HelloWorld
  },
  mounted() {
    function sleep(duration) {
      return new Promise(function (resolve, reject) {
        console.log("b");

        setTimeout(resolve, 1000);

        setTimeout(() => {
          console.log('d');
        }, 1000);
      })
    }
    
    console.log("a");
    sleep().then(() => {
      var begin = Date.now();
      while(Date.now() - begin < 1000);
      console.log("c");
    });
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
