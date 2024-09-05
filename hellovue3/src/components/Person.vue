<template>
    <div class="person">
        <h2>姓名：{{name}}</h2>
        <h2>年龄：{{age}}</h2>
        <button @click="xgname">修改名字</button>
        <button @click="xgage">修改年龄</button>
        <button @click="showtel">查看联系方式</button>
    </div>
</template>

<script lang="ts">
  export default {
    name:'Person'
  }
</script>

<script lang="ts" setup>
  import { ref } from 'vue'; 
    
  
      //数据
      let name = ref("张三")
      let age = ref(18)
      let tel = '19353088888'

      //方法
      function xgname (){
        name.value = 'zhang-san'
      }
      function xgage (){
        age.value += 1
      }
      function showtel (){
        alert(tel)
      }

</script>


<style>

  .person {
    background-color: rgb(11, 186, 234);
    border-radius: 10px;
    padding: 20px;
  }
  button {
    margin: 0px 5px;
  }

</style>