<template>
  <div>
    <form-helper>
      <!-- <h3 slot="title">Slot title</h3>
      <p slot="paragraph">Slot paragraph</p> -->
      <div slot="form-header">
        <h3>This is the title of the form</h3>
        <p>this is the paragraph of the form</p>
      </div>
      <div slot="form-fields">
        <input type="text" placeholder="your name" required />
        <input type="password" placeholder="password" required />
      </div>
      <div slot="form-control">
        <button type="submit" v-on:click="handleSubmit">Submit</button>
      </div>
    </form-helper>
  </div>
</template>

<script>
import formHelper from './components/formHelper.vue'


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
      alert('click')
    }
  }
}
</script>

<style>

</style>
