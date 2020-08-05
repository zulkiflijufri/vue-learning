<template>
  <div>
    <app-header v-bind:title="title" v-on:changeTitle="updateTitle($event)"/>
    <app-students v-bind:students="students"/>
    <app-footer v-bind:title="title"/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import Students from './components/Students.vue'

export default {
  components: {
    'app-header': Header,
    'app-footer': Footer,
    'app-students': Students
  },
  data () {
    return {
      students: [
        {name: 'Zulkifli', campus: 'Nurul Fikri', show: false},
        {name: 'Kalsum', campus: 'Unhas', show: false},
        {name: 'Yunita', campus: 'UNM', show: false},
        {name: 'Wiwi', campus: 'UIN', show: false},
        {name: 'Faiz', campus: 'IPB', show: false},
        {name: 'Fakhri', campus: 'ITB', show: false}
      ],
      // title: 'DaengCode'
      title: 'VuejsCode'
    }
  },
  methods: {
    updateTitle: function (newTitle) {
      this.title = newTitle
    }
  }
}
</script>

<style>

</style>
