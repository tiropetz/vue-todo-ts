<template>
  <div class="container">
    <div>
      <TaskRow
        v-for="todo in todoList"
        :key="todo.id"
        :title="todo.title"
        :is-checked="todo.isChecked"
      />
    </div>
  </div>
</template>

<script>
import TaskRow from "@/components/TaskRow.vue";
import Vue from "vue";

export default Vue.extend({
  name: "Home",
  components: {
    TaskRow
  },
  data() {
    return {
      todoList: [
        { id: 1, title: "aaaa", isChecked: true },
        { id: 2, title: "bbb", isChecked: true },
        { id: 3, title: "cc", isChecked: false }
      ]
    };
  }
});
</script>

<style scoped lang="scss">
.container {
  min-height: 100vh;
  background-color: #fafafa;
  padding: 15px;
  display: flex;
  justify-content: center;
}
</style>
