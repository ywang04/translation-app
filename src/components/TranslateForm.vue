<template>
 <div id="translateForm">
  <form v-on:submit="formSubmit">
   <input type="text" placeholder="Enter text" v-model="textToTranslate">
   <select v-model="language">
    <option value="zh">Chinese</option>
    <option value="fr">French</option>
    <option value="de">German</option>
    <option value="ja">Japanese</option>
    <option value="ko">Korean</option>
    <option value="es">Spanish</option>
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
      language: ''
    }
  },
  methods: {
    formSubmit: function (e) {
      this.$emit('formSubmit', this.textToTranslate, this.language)
      e.preventDefault()
    }
  },
  created: function () {
    this.language = 'zh'
  }
}
</script>
<style scoped>

</style>