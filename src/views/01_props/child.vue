<!--
 * @author: HuLuLin
 * @since: 2025-07-16
 * child.vue
-->
<script setup >
  import {ref, watchEffect, } from 'vue'
  const props = defineProps(['info','money'])
  const info = ref({})
  watchEffect(()=>{
    info.value = props
    console.log(info.value.info);
  })
</script>

<template>
  <div class="box">
    <p>我是子组件：测试接受父组件的数据</p>
    <p>{{ props.info }}</p>
    <p>{{ props.money }}</p>
    <p></p>
  </div>
</template>

<style lang="scss" scoped>
  .box{
    height: 200px;
    background: pink;
  } 
</style>
