<template>
  <div class="container">
    <div>
      <TaskRow
        v-for="todo in todoList"
        :key="todo.id"
        :id="todo.id"
        :title="todo.title"
        :deleteTask="deleteTask"
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
        { id: 1, title: "aaaa" },
        { id: 2, title: "bbb" },
        { id: 3, title: "cc" }
      ]
    };
  },
  methods: {
    deleteTask: function(id) {
      this.todoList = this.todoList.filter(todo => todo.id !== id);
    }
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
