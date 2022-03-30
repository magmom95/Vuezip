<template>
  <div class="menu">
    <a v-for="(test,i) in bar" :key="i">{{test}}</a>  
  </div>
  <img alt="Vue logo" src="./assets/logo.png">
  <div v-for="(a,i) in product" :key="i">
    <h4>{{product[i]}}</h4>
    <p>{{price[i]}}</p>
    <button @click="increase()">허위 매물신고</button>
    <br>
    <span>신고수 : {{신고수}}</span>
  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      price : ['15000','2324','1234'],
      product : ['1번째 상품', '2번째 상품', '3번째 상품'],
      bar : ['Home','Menu','Mypage'],
      신고수 : 0
    }
  },
    methods : {
      increase(){
        this.신고수 +=1
      }
    },
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

.menu {
  background : darkslateblue;
  padding : 15px;
  border-radius: 5px;
}

.menu a {
  color: white;
  padding: 10px;
}
</style>
