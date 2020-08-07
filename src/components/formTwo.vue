<template>
	<div>
    <form-helper>
      <div slot="form-header">
        <h3>Form Two - Log in</h3>
        <p>Enter your detail to login</p>
      </div>
      <div slot="form-fields">
        <input type="text" placeholder="your name" required />
        <input type="password" placeholder="password" required />
      </div>
      <div slot="form-control">
        <button type="submit" v-on:click="handleSubmit">Login</button>
      </div>
    </form-helper>
  </div>
</template>

<script>
import formHelper from './formHelper.vue'

export default {
  components: {
    'form-helper': formHelper
  },
	data () {
		return {

		}
	},
	methods: {
    handleSubmit: () => {

    }
	}

}
</script>

<style>

</style>