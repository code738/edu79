<template>
    <div class="person">
        <h2>这辆{{car.brand}},价值{{car.price}}万</h2>
        <button @click="xgjiage">修改价格</button>
        <button @click="xgpinpai">修改品牌</button>
        <br>
        <h2>列表</h2>
        <ul>
          <li v-for="yx in games" :key="yx.id">{{yx.name}}</li>
        </ul>
        <button @click="xgyx">修改第一个游戏</button>
    </div>
</template>

<script lang="ts">
  export default {
    name:'Car'
  }
</script>

<script lang="ts" setup>
    import { reactive,ref} from 'vue';

    // let games = reactive([
    //   {id:791,name:"原神"},
    //   {id:792,name:"逆战"},
    //   {id:793,name:"星铁"}
    // ])

      let games = ref([
      {id:791,name:"原神"},
      {id:792,name:"逆战"},
      {id:793,name:"星铁"}
    ])

    let car = ref({brand:"奔驰",price:100})

    // function xgjiage(){
    //     car.price += 10
    // }
    // function xgyx(){
    //   games[0].name = "七日世界"
    // }

    function xgjiage(){
        car.value.price += 10
    }
    function xgpinpai(){
      //Object.assign(car,{brand:"亚迪",price:1})
      car.value = {brand:"亚迪",price:1}
    }
    function xgyx(){
      games.value[0].name = "七日世界"
    }


</script>


<style>

  .person {
    background-color: rgb(11, 186, 234);
    border-radius: 10px;
    padding: 20px;
    margin-top: 10px;
  }
  button {
    margin: 0px 5px;
  }

</style>