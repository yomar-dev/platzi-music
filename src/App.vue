<template lang="pug">
  #app
    p(v-show="showValue") {{ value }}
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      msg: 'Hello World!!',
      showValue: true,
      value: 'Hello World!!'
    }
  }
}
</script>

<style lang="scss">
@import './scss/main.scss'
</style>
