![header](https://capsule-render.vercel.app/api?type=waving&color=auto&height=300&section=header&text=뷰%20정리%20&fontSize=90&animation=fadeIn&fontAlignY=38&desc=%20이성규&descAlignY=65&descAlign=90)

# 뷰 이것저것 정리

📌 리액트가 있는데 뷰를 쓰는 이유?

- 쉬워서 사용 (react와 달리 vue만의 새로운 문법 사용)

- Right-way가 존재

<details markdown="1">
<summary>✨ Right-way란?</summary>

- for 반목문을 사용하려 할때 (mpa, forEach, for in , for of 등 여러 반복문으로 사용가능하지만 vue는 v-for에 박아넣음

- 이로인해 협헙할 때 편리함

- 수정과 관리가 편함

---

</details>

- 속도가 빠름

---
<details markdown="1">
<summary>🎨 데이터 바인딩</summary>

<br>

```javascript
document.getElementById(test).innerHTML = 데이터;
```

- vue는 이럴 필요없이 데이터보관을 하고 HTML 꽂아넣음

```javascript
<script>
export default {
  name : 'App',
  data(){
    return {
      price1 : 60
    }
  }
}

</script>
```

- 로 데이터를 보관하고 

```javascript
<p>{{ price1 }} 원</p>
```

- 데이터를 꽂으면 됨

```javascript
<template>
  <div>
    <h4 :style="스타일">XX 원룸</h4>
    <p>XX 만원</p>
  </div>
  <div>
    <h4>XX 원룸</h4>
    <p>XX 만원</p>
  </div>
</template>

<script>
export default {
  name : 'App',
  data(){
    return {
      price1 : 60,
      스타일 : 'color:red'
    }
  }
}

</script>
```

- style="" id="" class="" 에도 데이터를 꽂을 수 있음

---

</details>

---

<details markdown="1">
<summary>🧨 v-for </summary>

<br>

```javascript
<div class="menu">
  <a v-for="test in 3" :key="test">Home</a>
</div>
```

- 원하는 태그에 v-for="작명 in 반복할횟수" 를 적음
 
- key 속성은 반복문돌릴 때 필요

- 위에 코드는 a태그가 3개 생성

```javascript
<div class="menu">
  <a v-for="test in subject" :key="test">{{ test }}</a>
</div>

data(){
  return {
    subject : ['Home', 'Shop', 'About']
  }
}
```

- subject안의 자료 갯수만큼 반복

- test는 반복될 때마다 subject 안에 있던 자료들

```javascript
<div class="menu">
  <a v-for="(test,i) in subject" :key="i"> {{ test }}</a>
</div>
```

- i 가 증가하면서 subject 안에 내용이 반복 출력

```javascript
<div v-for="(a,i) in products" :key="i">
  <h4>{{products[i]}}</h4>
  <p>50만원</p>
</div>
```

- 반복문을 돌리면서 products[i]를 상품명으로 출력

```javascript
<div>
  <h4>{{products[0]}}</h4>
  <p>50만원</p>
  <button @click="신고수++">허위매물신고</button>
  <span>신고수 : {신고수}</span>
</div>
```

- @click 을 통하여 data 상승

```javascript
<div>
  <h4>{{products[0]}}</h4>
  <p>50만원</p>
  <button @click="increase()">허위매물신고</button>
  <span>신고수 : {신고수}</span>
</div>
```

</details>

---

<details markdown="1">
<summary>🎃 v-if </summary>

<br>

```javascript
<div class="black-bg" v-if="모달창열렸나 == true">
  <div class="white-bg">
    <h4>상세페이지</h4>
    <p>상세페이지내용임</p>
  </div>
</div>
```

```javascript
data(){
  return {
    모달창열렸나 : true,
  }
}
```

- @click 버튼으로 on&&off 기능 가능

```javascript
<div v-for="(a, i) in 원룸들" :key="i">
  <img :src="a.image" class="room-img">
  <h4 @click="모달창열렸니 = true; 누른거 = i">{{a.title}}</h4>
  <p>{{a.price}}</p>
</div>
```
- v-else 라는 문법 존재

```javascript
<div v-if="1 == 2">
  안녕하세요
</div>
<div v-else>
  안녕하세요2
</div>
```

- else if 문법 가능

```javascript
<div v-if="1 == 2">
  안녕하세요
</div>
<div v-else-if="1 == 3">
  안녕하세요2
</div>
```

---

</details>

---
