<template>
  <li class="task-row">
    <input type="checkbox" v-model="isChecked" class="checkbox" />
    {{ title }}
  </li>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  name: "TaskRow",
  props: {
    title: { type: String, default: "No Title" },
    isChecked: { type: Boolean, default: false }
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
  align-items: center;
  padding: 0 20px;
  background-color: #fff;
  margin: 10px 0;
  box-shadow: 0 3px 6px rgba(0, 0, 0, 0.1);
}
.checkbox {
  margin-right: 16px;
}
</style>
