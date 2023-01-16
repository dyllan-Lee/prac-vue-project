<template>
  <div>
    <h1 class="h1">실험픽</h1>
  </div>
  <div class="cs">
    <h2>빨간줄이 생기는 이유를 알아보자</h2>
  </div>
</template>

<script>
export default {
name: 'SimpleThing',
  props: {
    msg: String
  }
}
</script>

<style scoped>
  .h1{
    font-size: 24px;
    border: 1px solid #333;
    color: blue;
  }
  .cs{
    margin-top: 30px;
  }
</style>