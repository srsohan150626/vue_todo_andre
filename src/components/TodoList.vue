<template>
  <div>
      <input type="text" placeholder="todo list input" class="todo-input"> 
      <span>todo list goes here</span>
  </div>
</template>

<script>
export default {
  name: 'todo-list',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
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

</style>
