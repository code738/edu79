<template>
    <div class="person">
        姓:<input type="text" v-model="xing"> <br>
        名:<input type="text" v-model="ming"> <br>
        全名:<span>{{qming}}</span> <br>
        <button @click="xgqm">修改全名</button>
    </div>
</template>

<script lang="ts">
  export default {
    name:'jisuan'
  }
</script>

<script lang="ts" setup>
    import { ref, computed } from 'vue';

    let xing = ref('')
    let ming = ref('')

    // let qming = computed(
    //     function(){
    //         return xing.value + ming.value
    //     }    
    // )
    let qming = computed({
        get(){
            return xing.value + ming.value
        },
        set(val){
            xing.value = val.charAt(0) 
            ming.value = val.charAt(1)
        }}
    )

    function xgqm(){
        qming.value = "李四"
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
    margin-top: 10px;
  }

</style>