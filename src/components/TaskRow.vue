<template>
  <li class="task-row">{{ title }}</li>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  name: "TaskRow",
  props: {
    title: { type: String, default: "No Title" }
  }
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.task-row {
  width: 100%;
  max-width: 800px;
  min-width: 500px;
  height: 50px;
  border-radius: 25px;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 0 20px;
  background-color: #fff;
  margin: 10px 0;
  box-shadow: 0 3px 6px rgba(0, 0, 0, 0.1);
}
</style>
