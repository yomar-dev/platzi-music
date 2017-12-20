<template lang="pug">
  #app
    img(src="./assets/logo.png")
    h1 {{ msg }}
    p {{ 3 * 4 }}
    p {{ 'Hola '  + 'Mundo!!'}}
    p {{ person.name + ' ' + person.lastname }}
    p {{ person.name.toUpperCase() }}
    p {{ JSON.stringify(person) }}
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      msg: 'Hello World!!',
      person: {
        name: 'Xavi',
        lastname: 'Hernandez'
      }
    }
  }
}
</script>

<style lang="scss">
@import './scss/main.scss'
</style>
