<template>
	<div>
    <form-helper>
      <div slot="form-header">
        <h3>Form One - Contact us</h3>
        <p>Fill in this form to contact us</p>
      </div>
      <div slot="form-fields">
        <input type="text" placeholder="name" required />
        <label>Message</label>
        <textarea cols="20" rows="2"></textarea>
      </div>
      <div slot="form-control">
        <button v-on:click="handleSubmit">Send</button>
      </div>
      <div slot="useful-links">
        <ul>
          <li><a href="#">Link -2</a></li>
          <li><a href="#">Link 2</a></li>
          <li><a href="#">Link 3</a></li>
          <li><a href="#">Link 4</a></li>
        </ul>
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