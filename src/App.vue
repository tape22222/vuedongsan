<template>
  <div class="black_bg" v-if="openModal">
    <div class="white_bg">
      <h4>상세 페이지</h4>
      <p>상세 페이지 내용</p>
      <button @click="openModal = false">닫기</button>
    </div>
  </div>
  <div class="menu">
    <a v-for="a in menudata" :key="a">{{a}}</a>
  </div>
  <!--<div v-for="(a, i) in products" :key="i">
    <img src="./assets/room0.jpg" class="room_img">
    <h4>{{products[i]}}</h4> or <h4>{{a}}</h4>
    <p>{{i + 5}}0 만원</p>
    <button @click="report[i]++">허위매물 신고</button>
    <span> 신고수: {{report[i]}}</span>
  </div>-->
  <div>
    <img src="./assets/room0.jpg" class="room_img">
    <h4 @click="openModal = true">{{products[0]}}</h4>
    <p>50 만원</p>
    <button @click="report[0]++">허위매물 신고</button>
    <span> 신고수: {{report[0]}}</span>
  </div>
  <div>
    <img src="./assets/room1.jpg" class="room_img">
    <h4>{{products[1]}}</h4>
    <p>60 만원</p>
    <button @click="report[1]++">허위매물 신고</button>
    <span> 신고수: {{report[1]}}</span>
  </div>
  <div>
    <img src="./assets/room2.jpg" class="room_img">
    <h4>{{products[2]}}</h4>
    <p>70 만원</p>
    <button @click="report[2]++">허위매물 신고</button>
    <span> 신고수: {{report[2]}}</span>
  </div>
</template>

<script>
export default {
  name: 'App',
  
  data() {
    return {
      openModal : false,
      menudata : ['Home', 'Shop', 'About'],
      report : [0, 0, 0],
      products : ['역삼동원룸', '천호동원룸', '마포구원룸'],
    }
  },

  methods : {
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
}

body {
  margin : 0;
}

div {
  box-sizing: border-box;
}

.black_bg {
  width: 100%;
  height: 100%;
  padding: 20px;
  background: rgba(0, 0, 0, 0.5);
  position: fixed;
}

.white_bg {
  widows: 100%;
  padding: 20px;
  border-radius: 8px;
  background: white;
}

.menu {
  padding: 15px;
  border-radius: 5px;
  background: darkslateblue;
}

.menu a {
  padding: 10px;
  color: white;
}

.room_img {
  width: 100%;
  margin-top: 40px;
}
</style>
