<template>
  <div>
    <h1>this is form tags</h1>
  </div>
  <div>
    <label for="text">text : </label>
    <input type="text" name="text" id="text" v-model="text"/>
  </div>
  <div v-for="ch in checked" v-bind:key="ch">
    <label> {{ch}} : </label>
    <input type="checkbox" v-model="reacti.ch" v-bind:value="ch"/>
  </div>
    <!-- <input type="checkbox" value="ch1" v-model="checked"/>
    <input type="checkbox" value="ch2" v-model="checked"/>
    <input type="checkbox" value="ch3" v-model="checked"/> -->
  <div v-for="ra in radio" v-bind:key="ra">
    <label> {{ra}} : </label>
  <input type="radio"  v-model="reacti.ra" v-bind:value="ra"/>
  </div>
  <div>
    <label>radio  O : </label>
    <input type="radio" v-model="reacti.OX" value="O">
    <label>radio  X : </label>
    <input type="radio" v-model="reacti.OX" value="X">
  </div>
  <!-- <input type="radio" />
  <input type="radio" />
  <input type="radio" />
  <input type="radio" /> -->
  <div>
  <textarea name="" id="" cols="30" rows="10" v-model="textA"></textarea>
  </div>
  <div>
    <select name="" id="" v-model="reacti.op">
      <option v-for="op in option" v-bind:key="op">{{op}}</option>
    </select>
  </div>
  <p>{{reacti}}</p>
</template>
<script>
import {reactive} from "vue";

export default {
  // data(){
  //   return{
  //     text : "1495",
  //     checked : ['ch1','ch2','ch3'],
  //     radio : ['ra1','ra2','ra3','ra4','ra5'],
  //   }
  // }
  setup(){
    const text = "1495";
    const checked = ['ch1','ch2','ch3'];
    const radio = ['ra1','ra2','ra3','ra4','ra5'];
    const option= ['서울','부산','경기','제주'];
    const ch=["ch1"];
    const ra="";
    const OX="";
    const textA= "메모를 입력해주세요";
    const op =''
    const reacti = reactive({
      radio,
      ch,
      ra,
      OX,
      textA,
      op,
    })

    return{
      text,
      checked,
      radio,
      reacti,
      OX,
      option,
    }
  }
}
</script>

<style>

</style>
