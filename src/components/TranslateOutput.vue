<template>
 <div id="translateOutput">
  <h2>{{translatedText}}</h2>

 </div>
</template>

<script>
export default {
  props: {
    translatedText: {
      type: String,
      required: true
    }
  },
  name: 'translateOutput',
  data: function () {
    return {

    }
  }
}
</script>
<style scoped>

</style>