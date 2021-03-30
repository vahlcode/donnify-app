<template>
  <div class="list-items">
    <h3>My Tasks</h3>
    <ul class="tasks">
      <Task
        v-for="task in tasks"
        :key="task.id"
        :task="task"
        @change="handleChange"
      />
    </ul>
  </div>
</template>

<script>
import Task from './Task.vue'
export default {
  components: { Task },
  data() {
    return({
      tasks: [
        {
          id: 0,
          title: 'Design a components',
          done: true
        },
        {
          id: 1,
          title: 'Design a components',
          done: false
        },
        {
          id: 2,
          title: 'Design a components',
          done: true
        },
        {
          id: 3,
          title: 'Design a components',
          done: false
        },
        {
          id: 4,
          title: 'Design a components',
          done: true
        },
        {
          id: 5,
          title: 'Design a components',
          done: false
        },
      ]
    })
  },
  methods: {
    handleChange: function(id) {
      const task = [...this.tasks].filter(item => item.id === id)[0]
      task.done = !task.done
    }
  }
}
</script>

<style scoped>
.list-items {
  width: 40%;
  border-radius: 8px;
  overflow: hidden;
  padding: 50px 20px;
  background: #ffffff;
}
.list-items > h3 {
  margin-bottom: 25px;
}
.list-items > .tasks {
  box-shadow: 0 0 40px #e1f0ff;
}
</style>