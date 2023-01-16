<template>
  <div class="about">
    <h1>This is an about page</h1>
  </div>
  <div>
  <ul>
    <li v-for="ramen in ramens" :key="ramen">{{ramen.name}} : {{ramen.price}}</li>
  </ul>
</div>
<table>
  <tr>
    <th v-for="head in f_head" :key="head" >{{head}}</th>
  </tr>
  <tr v-for="f_list in snaks" :key="f_list">
    <td v-for="snack in f_list" :key="snack" v-bind:colspan="snack.colspan || 1">{{snack.data}}</td>
  </tr>
</table>
<div></div>
<img src="../assets/logo.png" alt="">
<HelloWorld msg="컴포넌트는 부속품이니 실험해볼것"/>
<SimpleThing msg='부속 실험중'/>
</template>
<script>
import HelloWorld from '@/components/HelloWorld.vue'
import SimpleThing from '../components/SimpleThing.vue'

export default {
  data(){
    return{
      ramens : [
        {
          name : 'ichiran',
          price : '1050Yen',
        },
        {
          name:'kinryu',
          price :'850Yen',
        },
        {
          name:'nipomen',
          price :'660Yen',
        },
        {
          name:'nuguri',
          price:'980Won',
        },
      ],
      f_head:['snak','snak','snak'],
      snaks :[[
        {
          data : 'Jjangu'
        },
        {
          data : 'Postick'
        },
        {
          data : 'pringles'
        },
      ],[
        {
          data : 'oreo'
        },
        {
          data : 'oreoOz'
        },
        {
          data : 'mentos'
        },
      ],
      [
        {
          data : 'riceCrispy', colspan :2
        },

        {
          data : 'snikers'
        },
      ]
      ],
      
    }
  },
    components: {
    HelloWorld,
    SimpleThing
  },
}
</script>

<style scoped>
  table,td,th{
    border : 1px solid red;
    padding: 20px;
    /* border-collapse: collapse; */
  }
</style>