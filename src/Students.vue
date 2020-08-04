<template>
  <div>
    <h1>List of Students</h1>
    <ul>
      <li v-for="student in students">{{student}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data () {
    return {
      students: ['Zulkifli', 'Kalsum', 'Fakhri', 'Jufri']
    }
  }
}
</script>

<style scoped>
h1 {
  color: salmon;
}
</style>
