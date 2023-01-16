<template>
  <img src="../assets/logo.png" alt="">
  <h1>스케줄 표 만들기</h1>
  <TdList />
</template>

<script>
import TdList from '@/components/TdList.vue'

export default {
  name: 'TodoList',
  components: {
    TdList,
  }

}
</script>

<style>

</style>