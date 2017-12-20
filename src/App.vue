<template lang="pug">
  #app
    .container
      div
        img(src="./assets/img/header.jpg")
        h2 Registro estación Platzi
      .form
        div
          label Nombre
          input(type="text" name="nombre" placeholde="")
        div
          label Apellido
          input(type="text" name="nombre" placeholde="")
        div
          label Cargo
          input(type="text" name="nombre" placeholde="")
        .text-right
          button.button-info Enviar
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      msg: 'Hello World!!'
    }
  }
}
</script>

<style lang="scss">
@import './scss/main.scss'
</style>
