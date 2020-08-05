<template>
  <div id="students">
    <ul>
      <li v-for="student in students"  v-on:click="student.show = !student.show">
        <h2>{{student.name}}</h2>
        <h3 v-show="student.show">{{student.campus}}</h3>
      </li>
    </ul>
    <button v-on:click="deleteStudent">Delete student</button>
  </div>
</template>

<script>
export default {
  props: ['students'],
  data () {
    return {

    }
  },
  methods: {
    deleteStudent: function () {
      this.students.pop()
    }
  },
  // lifecycle hooks
  beforeCreate () {
    alert('beforeCreate')
  },
  Create () {
    alert('create')
  },
  beforeMount () {
    alert('beforeMount')
  },
  mounted () {
    alert('mounted')
  },
  beforeUpdate () {
    alert('beforeUpdate')
  },
  updated () {
    alert('updated')
  }
}
</script>

<style scoped>
#students {
  width: 100%;
   max-width: 1200px;
   margin: 40px auto;
   padding: 0 20px;
   box-sizing: border-box;
}
ul {
  display: flex;
  flex-wrap: wrap;
  list-style-type: none;
  padding: 0;
}
li {
  flex-grow: 1;
  flex-basis: 300px;
  text-align: center;
  padding: 30px;
  border: 1px solid #222;
  margin: 10px;
}
</style>
