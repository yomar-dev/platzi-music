<template lang="pug">
  #app
    p(v-show="showValue") {{ value }}
    p(v-if="showValue") {{ value }}
    p(v-else) {{ 'Hola Mundo!!' }}
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      msg: 'Hello World!!',
      showValue: false,
      value: 'Hello World!!'
    }
  }
}
</script>

<style lang="scss">
@import './scss/main.scss'
</style>
