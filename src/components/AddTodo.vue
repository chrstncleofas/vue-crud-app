<template>
  <div class="container">
    <form @submit.prevent="addTodo">
      <input type="text" v-model="title" name="title" placeholder="Add Todo...">
      <input type="submit" value="Submit" class="btn">
    </form>
  </div>
</template>

<script>
// import uuid from 'uuid';
export default {
  name: "AddTodo",
  data() {
    return {
      title: ''
    }
  },
  methods: {
    addTodo() {
      const newTodo = {
        title: this.title,
        completed: false
      }
      // Send up to parent
      this.$emit('add-todo', newTodo);

      this.title = '';
    }
  }
}
</script>

<style scoped>
  form {
    display: flex;
    margin-left: 15px;
    margin-right: 15px;
  }

  input[type="text"] {
    flex: 10;
    padding: 5px;
    margin-bottom: 9px;
    border: none;
    margin-right: 3px;
  }

  input[type="submit"] {
    flex: 2;
    margin-bottom: 9px;
  }

  .btn {
    display: inline-block;
    border: none;
    background-color: #0d7748;
    color: #fff;
    padding: 7px 18px;
    cursor: pointer;
  }

  .btn:hover {
    background-color: #42b983;
  }
</style>


