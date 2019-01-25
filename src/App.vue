<template>
  <div id="app">
    <div class="container">
      <TodoInput></TodoInput>
      <TodoOutput></TodoOutput>
    </div>
  </div>
</template>


<script>
import TodoOutput from "./components/TodoOutput.vue";
import TodoInput from "./components/TodoInput.vue";

export default {
  name: "app",
  components: {
    TodoOutput,
    TodoInput
  }
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  font-family: Arial, 宋体;
}
html,
body {
  width: 100%;
  height: 100%;
}
#app {
  width: 100%;
  height: 100%;
  background-color: #edf5f8;
  display: flex;
  justify-content: center;
  align-items: center;
}
.container {
  width: 60%;
  height: 60%;
  padding: 30px;
  background-color: #fff;
  box-shadow: 0 10px 12px #bbb;
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>


