<template>
    <div class="a11">
        <h1>你好世界！</h1>
        <Person></Person>
    </div>
</template>

<script lang="ts">
  import Person from './components/Person.vue';
  
  export default {
    name:'APP', //组件名
    components:{Person}  //注册组件
  }
</script>

<style>

.a11{
    background-color: aquamarine;
    border-radius: 10px;
    padding: 20px;
}

</style>

