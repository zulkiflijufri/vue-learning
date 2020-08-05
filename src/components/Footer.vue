<template>
  <footer>
    <p>{{ copyright }} {{ title }}</p>
  </footer>
</template>

<script>
import { bus } from '../main';

export default {
  props: {
    title: {
      type: String
    }
  },
  data () {
    return {
      copyright: 'Copyright 2020'
    }
  },
  created () {
    bus.$on('titleChange', (data) => {
      this.title = data
    }) // event bus
  }
}
</script>

<style scoped>
footer {
  background-color: #222;
  padding: 6px;
}
p {
  color: lightgreen;
  text-align: center;
}
</style>
