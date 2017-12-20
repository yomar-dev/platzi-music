<template lang="pug">
  #app
    p(v-show="showValue") {{ value }}
    p(v-if="showValue") {{ value }}
      span Mensaje
    p(v-else) {{ 'Hola Mundo!!' }}

    ul
      li(v-for="i in items") {{ i }}

    input(v-model="name" placeholder="Ingresa tu nombre")
    p {{ name }}
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      msg: 'Hello World!!',
      showValue: false,
      value: 'Hello World!!',
      items: [1, 2, 3, 4],
      name: ''
    }
  }
}
</script>

<style lang="scss">
@import './scss/main.scss'
</style>
