<template>
  <div>
      <input type="text" placeholder="todo list input" class="todo-input" v-model="newTodo" @keyup.enter="addTodo"> 
      <div v-for="(todo,index) in todos" :key="todo.id" class="todo-item"> 
        <div>
          {{todo.title}}
        </div>
        <div class="remove-item" @click="removeTodo(index)">
          &times;
        </div>
      </div>
     
  </div>
</template>

<script>
export default {
  name: 'todo-list',
  data () {
    return {
      newTodo: '',
      idForTodo: 3,
      todos: [
        {
          'id': 1,
          'title': 'Finish the Project',
          'completed' : false
        },
        {
          'id': 2,
          'title': 'Finish the Medicine',
          'completed' : false
        },
      ]
    }
  },
  methods: {
    addTodo() {
      if(this.newTodo.trim().length == 0){
        return
      }
      this.todos.push({
        id: this.idForTodo,
        title: this.newTodo,
        completed: false,
      })
      this.newTodo = ''
      this.idForTodo++
    },
    removeTodo(index){
      this.todos.splice(index, 1)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style >
.todo-input{
    width: 100%;
    padding: 10px 10px;
    margin-bottom: 16px;
    font-size: 18px;
}

.todo-item{
  margin-bottom: 12px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.remove-item {
  cursor: pointer;
  margin-left: 14px;
}

</style>
