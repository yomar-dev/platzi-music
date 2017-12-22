<template lang="pug">
  #app
    section.section
      nav.nav.has-shadow
        .container
          .field.has-addons
            .control.is-expanded
              input.input.is-large(
                type="text",
                placeholder="Buscar canciones",
                v-model="searchQuery"
              )
            .control
              a.button.is-info.is-large Buscar
            .control
              a.button.is-danger.is-large &times;

      .container
        .columns
          .column
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      searchQuery: ''
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
    search () {
      console.log(this.searchQuery)
    }
  }
}
</script>

<style lang="scss">
@import './scss/main.scss'
</style>
