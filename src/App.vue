<template>
 <div id="app">
  <h1>Online Translation</h1>
  <h5>Simple / Easy to Use / Convenient</h5>
  <translateForm v-on:formSubmit="translateText"></translateForm>
  <translateOutput v-bind:translatedText="translatedText"></translateOutput>
 </div>
</template>

<script>
import TranslateForm from './components/TranslateForm'
import TranslateOutput from './components/TranslateOutput'

export default {
  name: 'App',
  data: function () {
    return {
      translatedText: ''
    }
  },
  components: {
    TranslateForm,
    TranslateOutput
  },
  methods: {
    translateText: function (text, language) {
      const baseurl = 'https://translate.yandex.net/api/v1.5/tr.json/translate?key=trnsl.1.1.20180211T012317Z.e40553e0346713a2.e8d100804e1839c82cc4f0a882aed8f01799f9fc&lang='
      const url = baseurl + language + '&text=' + text
      console.log(url)
      this.$http.get(url).then((response) => {
        this.translatedText = response.body.text[0]
      })
    }
  }
}
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
