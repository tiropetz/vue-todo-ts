<template>
  <li class="task-row">
    {{ title }}
    <button @click="deleteTask(id)">完了</button>
  </li>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  name: "TaskRow",
  props: {
    id: { type: String },
    title: { type: String, default: "No Title" },
    deleteTask: { type: Function }
  }
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.task-row {
  width: 200px;
  max-width: 800px;
  min-width: 500px;
  height: 50px;
  border-radius: 25px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 20px;
  background-color: #fff;
  margin: 10px 0;
  box-shadow: 0 3px 6px rgba(0, 0, 0, 0.1);
}
</style>
