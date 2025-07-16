<script setup lang="ts">
  import { RouterLink, RouterView } from 'vue-router'
  import {ref,} from 'vue'

  import { useRoute, useRouter } from 'vue-router'

  const router = useRouter()
  const route = useRoute()
  // 定义数组的类型
  interface arrayType {
    id: string,
    name: string
  }

  const array = ref<arrayType[]>([ 
    {
      id: '001',
      name: 'props'
    },
    {
      id: '002',
      name: 'custom-event'
    },
    {
      id: '003',
      name: 'event-bus'
    },
    {
      id: '004',
      name: 'v-model'
    },
    {
      id: '005',
      name: 'attrs-listeners'
    },
    {
      id: '006',
      name: 'ref-children-parent'
    },
    {
      id: '007',
      name: 'provide-inject'
    },
    {
      id: '008',
      name: 'pinia(vuex)'
    },
    {
      id: '009',
      name: 'slots'
    },

  ])

  const handleById = (id: String)=>{
    switch(id){
      case '001':{
        router.push('/props')
        break;
      }
      case '002':{

      }
      case '003':{
        
      }
      case '004':{
        
      }
      case '005':{
        
      }
      case '006':{
        
      }
      case '007':{
        
      }
      case '008':{
        
      }
      case '009':{
        
      }
      case '002':{
        
      }
    }
  }
</script>

<template>
  <div class="wapper">
    <div class="title">
      vue3的常用组件通信方式
    </div>
    <div class="content">
      <button class="content-button" v-for="item in array" :key="item.id" @click="handleById(item.id)">{{ item.name }}</button>
    </div>
    <RouterView />
  </div>
</template>

<style lang="scss" scoped>
  .wapper{
    padding: 10px;
    .title{
      font-size: 20px;
      display: flex;
      justify-content: center;
      margin-bottom: 10px;
    }
    .content{
      background-color: pink;
      padding: 10px;
      &-button{
        margin-right: 5px;
      }
    }
  }
</style>
