<template>
  <div class="menu">
    <a v-for="(test,i) in bar" :key="i">{{test}}</a>  
  </div>
  <img alt="Vue logo" src="./assets/logo.png">
  <div v-for="(a,i) in product" :key="i">
    <h4 @click="modal=true">{{product[i]}}</h4>
    <p>{{price[i]}}</p>
    <button @click="increase()">허위 매물신고</button>
    <br>
    <span>신고수 : {{신고수}}</span>
  </div>
  <div class="black-bg" v-if="modal == true">
    <div class="white-bg">
      <h4>상세페이지</h4>
      <p>상세페이지 내용</p>
    </div>
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
      신고수 : 0,
      modal : false,
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

body {
  margin : 0
}

div {
  box-sizing: border-box;
}

.black-bg{
  width: 100%; height:100%;
  background: black;
  position: fixed;
  padding: 20px;
}
.white-bg{
  width: 100%; 
  background: white;
  position: fixed;
  padding: 20px;
}
</style>
