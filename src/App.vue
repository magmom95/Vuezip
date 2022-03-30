<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <div>
    <h4 :style="test">{{product[0]}}</h4>
    <p>{{price[0]}}</p>
  </div>
  <div>
      <h4>{{product[1]}}</h4>
      <p>{{price[1]}}</p>
  </div>
  <div>
      <h4>{{product[2]}}</h4>
      <p>{{price[2]}}</p>
  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      price : ['15000','2324','1234'],
      product : ['1번째 상품', '2번째 상품', '3번째 상품'], 
      test : 'color:red'
    }
  },
  components: {

  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
