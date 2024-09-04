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
    name:'Person' //组件名
    ,
    data(){
      return {
        name:"张三",
        age:18,
        tele:"193588888888"
      }
    },
    methods:{
      showtel(){
        alert(this.tele)
      },
      xgname(){
        this.name = "zhengsan"
      },
      xgage(){
        this.age += 1
      }
    }

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