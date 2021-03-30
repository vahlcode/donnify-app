<template>
  <li class="list-item" :class="task.done ? 'done' : ''" @click="handleClick">
    {{ task.title }}
  </li>
</template>

<script>
export default {
  props: ['task'],
  methods: {
    handleClick: function() {
      this.emitChange()
    },
    emitChange: function() {
      const id = this.task.id
      this.$emit('change', id)
    }
  }
}
</script>

<style scoped>
.list-item {
  cursor: pointer;
  position: relative;
  padding: 10px 15px 10px 45px;
  border-bottom: 1px solid #f1f1f1;
  background: #ffffff;
  font-size: 15px;
  list-style: none;
  text-decoration: none;
  transition: .5s;
}
.list-item.done {
  text-decoration: line-through;
}
.list-item:last-of-type {
  border-bottom: none;
}
.list-item::before {
  content: '';
  height: 15px;
  width: 15px;
  border-radius: 50%;
  background: #eff7ff;
  transition: .5s;
  position: absolute;
  left: 15px;
  top: 10px;
}
.list-item.done::before {
  background: #268aee;
}
</style>
