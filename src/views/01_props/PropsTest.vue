<!--
 * @author: HuLuLin
 * @since: 2025-07-16
 * parent.vue
-->
<script setup >
  import Child from './child.vue'
  import {ref} from 'vue'
  const money = ref(1000)
</script>

<template>
  <div class="container"> 
    <h1> props: 我是父组件</h1>
    <hr/>
    <Child info="我是父组件传递给子组件的信息" :money="money"></Child>
  </div>
</template>

<style lang="scss" scoped>
.container {
  width: 100vw;
  height: 400px;
  background: yellowgreen;
}
</style>