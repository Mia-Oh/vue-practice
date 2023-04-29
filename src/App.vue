<template>
  <img alt="logo" class="logo" src="./assets/logo.png">
  <div>
    <img src="./assets/pil0.gif" class='pil-img'>
    <h4>{{posts[0]}} 피리미리</h4>
    <p>{{comments[0]}}</p>
    <span>{{likeCount[0]}}</span>
    <button @click="likeCount[0]+=1">❤️</button>
  </div>
  <div>
    <img src="./assets/pil1.gif" class='pil-img'>    
    <h4>{{posts[1]}} 피리미리</h4>
    <p>{{comments[1]}}</p>
    <span>{{likeCount[1]}}</span>
    <button @click="likeCount[1]+=1">❤️</button>
  </div>
  <div>
    <img src="./assets/pil2.gif" class='pil-img'>
    <h4>{{posts[2]}} 피리미리</h4>
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
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.logo {
  width: 10%;
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
