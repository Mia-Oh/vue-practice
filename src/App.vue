<template>
  <!-- 모달창 -->
  <div class="black-bg" v-if="isOpenModal == true">
    <div class="white-bg" @click="isOpenModal = false">
      <h4>Oepn Modal</h4>
      <p>Hi! It's me! Modal~!</p>
  </div>
  </div>
  <img alt="logo" class="logo" src="./assets/logo.png">
  <div>
    <img src="./assets/pil0.jpg" class='pil-img'>
    <h4 @click="isOpenModal = true">{{posts[0]}} 피리미리</h4>
    <p>{{comments[0]}}</p>
    <span>{{likeCount[0]}}</span>
    <button @click="likeCount[0]+=1">❤️</button>
  </div>
  <div>
    <img src="./assets/pil1.jpg" class='pil-img'>    
    <h4 @click="isOpenModal = true">{{posts[1]}} 피리미리</h4>
    <p>{{comments[1]}}</p>
    <span>{{likeCount[1]}}</span>
    <button @click="likeCount[1]+=1">❤️</button>
  </div>
  <div>
    <img src="./assets/pil2.jpg" class='pil-img'>
    <h4 @click="isOpenModal = true">{{posts[2]}} 피리미리</h4>
    <p>{{comments[2]}}</p>
    <span>{{likeCount[2]}}</span>
    <button @click="likeCount[2]+=1">❤️</button>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      isOpenModal : false,
      likeCount : [0,0,0],
      posts : ['머찐','여름','깨물하트'],
      comments: ['너무 멋있어여','아주 사랑스러워요','커아이~'],
    }
  },
  components: {
  }
}
</script>

<style>
* {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
body {
  margin : 0;
}
div {
  box-sizing: border-box;
  margin: 0 0 50px 0;
}
h4,button {
  cursor: pointer;
}
.black-bg {
  display: flex;
  align-items: center;
  width: 100%;
  height: 100%;
  background: rgba(0,0,0,0.5);
  position: fixed;
  padding: 20px;
}
.white-bg {
  width: 100%;
  background: #fff;
  border-radius: 10px;
  padding: 20px;
  cursor: pointer;
}
.logo {
  width: 10%;
  margin-top: 50px;
}
span {
  margin-right: 1rem;
}
button {
  background: none;
  border: none;
  font-size: 1.2rem;
}
.pil-img {
  width: 30rem;
  margin-top: 100px;
}
</style>
