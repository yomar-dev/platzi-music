<template lang="pug">
  #app
    p(v-show="showValue") {{ value }}
    p(v-if="showValue") {{ value }}
    p(v-else) {{ 'Hola Mundo!!' }}

    ul
      li(v-for="i in items") {{ i }}
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      msg: 'Hello World!!',
      showValue: false,
      value: 'Hello World!!',
      items: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
    }
  }
}
</script>

<style lang="scss">
@import './scss/main.scss'
</style>
