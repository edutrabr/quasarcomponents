<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <li>
    <div>{{task.name}} [{{task.id}}]</div>
    <small>{{task.dueDate}} @ {{task.dueTime}}</small>
    <button @click="deleteTask(task.id)">X</button>
  </li>
</template>

<script>
export default {
  // name: 'ComponentName',
  props: {
    task: {
      type: Object,
      required: true
    }
  }
}
</script>
