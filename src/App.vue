
<!--
⣿⣿⣿⣿⣿⣿⢟⣡⣴⣶⣶⣦⣌⡛⠟⣋⣩⣬⣭⣭⡛⢿⣿⣿⣿⣿
⣿⣿⣿⣿⠋⢰⣿⣿⠿⣛⣛⣙⣛⠻⢆⢻⣿⠿⠿⠿⣿⡄⠻⣿⣿⣿ 
⣿⣿⣿⠃⢠⣿⣿⣶⣿⣿⡿⠿⢟⣛⣒⠐⠲⣶⡶⠿⠶⠶⠦⠄⠙⢿ 
⣿⠋⣠⠄⣿⣿⣿⠟⡛⢅⣠⡵⡐⠲⣶⣶⣥⡠⣤⣵⠆⠄⠰⣦⣤⡀ 
⠇⣰⣿⣼⣿⣿⣧⣤⡸⢿⣿⡀⠂⠁⣸⣿⣿⣿⣿⣇⠄⠈⢀⣿⣿⠿ 
⣰⣿⣿⣿⣿⣿⣿⣿⣷⣤⣈⣙⠶⢾⠭⢉⣁⣴⢯⣭⣵⣶⠾⠓⢀⣴
⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣉⣤⣴⣾⣿⣿⣦⣄⣤⣤⣄⠄⢿⣿
⣿⣿⣿⣿⣿⣿⣿⣿⠿⠿⠿⠿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣇⠈⢿
⣿⣿⣿⣿⣿⣿⡟⣰⣞⣛⡒⢒⠤⠦⢬⣉⣉⣉⣉⣉⣉⣉⡥⠴⠂⢸
⠻⣿⣿⣿⣿⣏⠻⢌⣉⣉⣩⣉⡛⣛⠒⠶⠶⠶⠶⠶⠶⠶⠶⠂⣸⣿
⣥⣈⠙⡻⠿⠿⣷⣿⣿⣿⣿⣿⣿⣿⣿⣿⣾⣿⠿⠛⢉⣠⣶⣶⣿⣿
⣿⣿⣿⣶⣬⣅⣒⣒⡂⠈⠭⠭⠭⠭⠭⢉⣁⣄⡀⢾⣿⣿⣿⣿⣿⣿
            镇楼专用！
-->








<template>
  <div id="app">
    
    <!-- 例子1 -->
    <!-- 
      <img alt="Vue logo" src="./assets/logo.png">
      <nav>
      <button class="btn" @click="tran('Index')">首页</button>
      <button class="btn" @click="tran('List')">列表</button>
      <button class="btn" @click="tran('Form')">表单</button>
    </nav> 
    
    <component :is="com">

    </component>  -->

    <!-- 例子2 -->
    <nav>
      <ul>
        <li @click="tran('Index')">首页</li>
        <li @click="tran('List')">列表</li>
        <li @click="tran('Form')">表单</li>
      </ul>
    </nav>
    <div class="container">
      <!-- 内容显示区域 -->
      <component :is="com"></component>
    </div>
    
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
// import Index from './view/Index.vue'
// import Form from './view/Form.vue'
// import List from './view/List.vue'

export default {
  name: 'app',
  components: {
    HelloWorld,
    Index,
    Form,
    List
  },
  data: function(){
    return {
      com:'Index'
    }
  },
  methods:{
    // tran1(){
    //   this.com = 'Index'
    // },
    // tran2(){
    //   this.com = 'List'
    // },
    // tran3(){
    //   this.com = 'Form'
    // }
    // 以上为 定义的三个方法 然后在每个按钮执行一个方法 


    // tran()里面传进来的name 为各条button里面的字符串
    tran(name){
      this.com = name
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  width: 1200px;
  margin: 0 auto;
  height: 600px;
}
nav .btn{
  margin-right: 20px;
}
#app nav{
  width: 30%;
  float: left;
  /* background-color: yellow; */
}
#app nav ul li{
  line-height: 50px;
  height: 50px;
  background-color: #334455;
  color: #fff;
}
.container{
  margin-left: 32%;
  /* background-color: gray; */
  border: 1px solid #888;
}
</style>
