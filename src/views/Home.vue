<template>
  <div class="container">
    <div class="wrapper">
      <h1>TODO LIST</h1>
      <TaskRow
        v-for="task in todoList"
        :key="task.id"
        :id="task.id"
        :title="task.title"
        :deleteTask="deleteTask"
      />
    </div>
    <div class="wrapper">
      <h1>DONE TASKS</h1>
      <div v-for="task in doneList" :key="task.id">{{ task.title }}</div>
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
      ],
      doneList: []
    };
  },
  methods: {
    deleteTask: function(id) {
      this.doneList = [
        ...this.doneList,
        this.todoList.find(task => task.id === id)
      ];
      this.todoList = this.todoList.filter(task => task.id !== id);
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
.wrapper {
  margin: 0 20px;
}
</style>
