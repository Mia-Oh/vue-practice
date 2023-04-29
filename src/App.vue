<template>
  <img alt="logo" src="./assets/logo.png">
  <div>
    <h4>{{products[0]}} 원룸</h4>
    <p>{{price1}} 만원</p>
    <span>신고 : {{신고수}}</span>
    <button @click="신고수+=1">허위 매물 신고</button>
  </div>
  <div>
    <h4>{{products[1]}} 원룸</h4>
    <p>{{price2}} 만원</p>
  </div>
  <div>
    <h4>{{products[3]}} 원룸</h4>
    <p>{{price2}} 만원</p>
  </div>  
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      신고수 : 0,
      products : ['역삼동','천호동','남영동'],
      price1: 60,
      price2 : 90,
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
img {
  width: 10%;
}
span {
  margin-right: 1rem;
}
</style>
