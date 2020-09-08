<template>
  <div class="container">
    <div>
      <TaskRow title="へいへい！" isChecked />
      <TaskRow title="xxをやる" />
      <TaskRow title="これがタスク" />
    </div>
  </div>
</template>

<script>
import TaskRow from "@/components/TaskRow.vue";

export default {
  name: "Home",
  components: {
    TaskRow
  }
};
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
