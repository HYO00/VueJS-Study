<template>

  <div class="menu">
    <a v-for="작명 in subbar" :key="작명">{{작명}}</a>
  </div>
  
  <div v-for="(list, i) in 3" :key="i">
    <h4 :style="스타일">{{products[i]}}</h4>
    <p >{{price[i]}} 만원</p>
    <button @click="increase(i)">상세보기</button>
    <span>likes : {{like[i]}}</span>
  </div>
 
</template>

//js
<script>


export default {
  name: 'App',
  //data보관통
  data(){
    return {
      //여기에 데이터 보관 변수같은거 데이터는 object 자료로 저장 {데이터이름: 데이터내용}
      like:[0,0,0],
      price: [5,8,14],
      products: ['자켓', '맨투맨', "후드집업"],
      subbar:["home","menu","about"],
      스타일: 'color: blue',
     
    }
  },
  methods:{
    increase(i){
			this.like[i]++
      console.log("click")
		}
  },
  components: {
  }
}
</script>

//css
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-bottom: 20px;

}

.menu {
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;
}
.menu a{
  color: white;
  padding: 10px;
}
</style>
