<template>
  <input
    class="todo-input"
    placeholder="从这里添加一个新的待办事项"
    v-model.trim="todoContent"
    @keyup.enter="add"
  >
</template>

<script>
import { ADD_TODO } from "../state/state";
export default {
  name: "TodoInput",
  data() {
    return {
      todoContent: ""
    };
  },
  methods: {
    add() {
      if (this.todoContent === "") {
        return false;
      }
      //存储在Store中
      this.$store.commit(ADD_TODO, this.todoContent);
      //清空Input中的值
      this.todoContent = "";
    }
  }
};
</script>

<style lang="scss">
.todo-input {
  width: 60%;
  height: 35px;
  padding: 0 10px;
  font-size: 14px;
  border: 3px solid #c4e3ef;
  border-radius: 50px;
  outline: none;
}
</style>