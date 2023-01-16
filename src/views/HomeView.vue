<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <SimpleThing/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import SimpleThing from '@/components/SimpleThing.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld,
    SimpleThing
  }
}
</script>
