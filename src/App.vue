<template lang="pug">
  #app
    section.section
      nav.nav.has-shadow
        .container
          input.input.is-large(type="text", placeholder="Buscar canciones")
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
    }
  },
  /**
   * Computed Properties
   * Son funciones que devuelven un valor y dentro de estas funciones
   * puedo utilizar funciones ya existentes.
   */
  computed: {
  },
  /**
   * Nos permite ejecutar código a partir de que una propiedad de nuestro
   * view model cambia. A diferencia de las Computed Properties no devuelven
   * un valor, no son propiedades y tampoco pueden ser utilizadas en expresiones.
   * 
   * NOTA: los watchers se enlazan directamente sobre una variable del view model,
   * por lo cual se tienen que llamar de la misma manera, al igual que las
   * computed properties son funciones.
   */
  watch: {
  },
  methods: {
  }
}
</script>

<style lang="scss">
@import './scss/main.scss'
</style>
