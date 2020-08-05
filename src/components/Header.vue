<template>
	<header>
		<h1 v-on:click="changeTitle">{{ title }}</h1>
	</header>
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
    	// title: 'Vue Playlist'
    }
  },
  methods: {
  	changeTitle: function () {
  		// this.$emit('changeTitle', 'DaengCode'); // event child to parent
  		this.title = 'DaengCode'
  		bus.$emit('titleChange', 'DaengCode'); // event bus
  	}
  }
}
</script>

<style scoped>
header {
	background-color: lightgreen;
	padding: 10px;
}
h1 {
	color: #222;
	text-align: center;
}
</style>
