<template>
  <div>
    <input type="date" v-model="todoDate" /> | 
    <input type="text" v-model="todoPlace"/>
    <button @click="addTodo">add</button>
  </div>
  <ul>
    <li v-for="(todo, index) in todolist" :key="todo" @click="complete(todo, index)" v-bind:class='{completed : todo.complete}'>{{index+1}} . {{todo}},{{todo.item}}{{todo.complete}}
      <span @click="removeTodo(todo, index)">삭제</span>
    </li>
  </ul>
<div></div>

</template>

<script>
export default {
  data : function(){
    return{
      todoDate :"",
      todoPlace :"",
      todolist:[],
    };
  },
  methods : {
    addTodo : function(){
      console.log(this.todoPlace)
      if(this.todoPlace != ""){
        let obj = {dates : this.todoDate, place: this.todoPlace , complete : false};
          localStorage.setItem(this.todoPlace, JSON.stringify(obj));
          console.log(obj);
        this.todolist.push(obj);
        this.todoDate ="";
      }
    },
    removeTodo: function(todo, index){
      localStorage.removeItem(todo.place);
      this.todolist.splice(index, 1);
    },
    complete:function(todo,index){
      todo.complete = !todo.complete;
      localStorage.removeItem(todo);
      localStorage.setItem(this.todo.place, JSON.stringify(todo));
      console.log(todo);
    },
  },
  created : function(){
    if(localStorage.length>0){
      for(var i = 0; i<localStorage.length; i++){
        if(localStorage.key(i) !=="loglecel:webpack-dev-server"){
          this.todolist.push(JSON.parse(localStorage.getItem(localStorage.key(i))));
        }
      }
    }
  },
};
</script>

<style scoped>
  .completed{
    background-color: chocolate;
  }
</style>