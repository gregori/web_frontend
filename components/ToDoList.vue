<template>
  <div class="to-do-container">
    <div class="create-container">
      <input v-model="titleOfNewToDo" type="text">
      <button @click="create">
        Add
      </button>
    </div>
    <div class="to-do-list-container" />
  </div>
</template>

<script>
export default {
  name: 'ToDoList',
  props: {
    todos: {
      type: Array,
      default () {
        return []
      }
    }
  },
  data () {
    return {
      titleOfNewToDo: ''
    }
  }
}
</script>

<style lang="scss">
.to-do-container {
  width: 400px;
  margin: 50px auto auto;
  display: block;

  .create-container {
    width: 100%;
    height: 50px;
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);

    input {
      height: 50px;
      width: 250px;
      border: none;
      padding-left: 10px;
      font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
        Roboto, 'Helvetica Neue', Arial, sans-serif;
      font-size: 18px;
      &:focus {
        outline: none;
      }
    }

    button {
      height: 45px;
      float: right;
      background: none;
      width: auto;
      margin: 0;
      border: none;
      cursor: pointer;
      text-align: right;
      padding-right: 20px;
      font-size: 18px;
      &:focus {
        outline: none;
      }
    }
  }
}

.to-do-list-container {
  width: 400px;
  margin: 50px auto auto;
  display: block;
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
}

</style>
