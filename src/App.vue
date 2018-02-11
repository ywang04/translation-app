<template>
 <div id="app">
  <h1>Online Translation</h1>
  <h5>Simple / Easy to Use / Convenient</h5>
  <translateForm></translateForm>
  <translateOutput></translateOutput>
 </div>
</template>

<script>
import TranslateForm from './components/TranslateForm'
import TranslateOutput from './components/TranslateOutput'
export default {
  name: 'App',
  data: function () {
    return {
    }
  },
  components: {
    TranslateForm,
    TranslateOutput

  }
}
</script>

<style>

</style>
