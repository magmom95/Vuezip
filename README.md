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
