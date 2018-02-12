<template>
 <div id="translateOutput">
  <p>{{translatedText}}</p>

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