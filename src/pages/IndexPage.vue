<template>
  <q-page>
    <ul>
      <task v-for="(task, index) in tasks"
        :task="task"
        :key="index"
      >
      </task>
    </ul>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue'
import Task from 'components/task.vue'

export default defineComponent({
  name: 'IndexPage',
  components: { Task },
  data() {
    return {
      tasks: [
        {
          'id': 1,
          'name': 'Comprar bananas',
          'dueDate': '10/04/2024',
          'dueTime' : '18:00'
        },
        {
          'id': 2,
          'name': 'Ir ao shopping',
          'dueDate': '10/04/2024',
          'dueTime' : '19:00'
        },
        {
          'id': 3,
          'name': 'Code Vue',
          'dueDate': '10/04/2024',
          'dueTime' : '22:00'
        }
      ]
    }
  },
  methods: {
    deleteTask(index) {
      this.tasks.splice(index, 1)
    }
  }
})
</script>
