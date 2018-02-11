<template>
 <div id="translateForm">
  <form v-on:submit="formSubmit">
   <input type="text" placeholder="Enter text" v-model="textToTranslate">
   <select>
    <option value="en">English</option>
   </select>
   <!-- <input type="submit" value="Translate"> -->
   <button type="submit">Translate</button>
  </form>
 </div>
</template>

<script>
export default {
  name: 'translateForm',
  data: function () {
    return {
      textToTranslate: '',

    }
  },
  methods: {
    formSubmit: function (e) {
      // alert(this.textToTranslate)
      this.$emit('formSubmit', this.textToTranslate)
      e.preventDefault()
    }
  }
}

</script>
<style scoped>

</style>