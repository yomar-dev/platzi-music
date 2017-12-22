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
              a.button.is-info.is-large(@click="search") Buscar
            .control
              a.button.is-danger.is-large &times;
          p
            small {{ searchMessage }}

      .container
        .columns
          .column(v-for="t in tracks") {{ t.name }} - {{ t.artist }}
</template>

<script>

const tracks = [
  { name: 'Los caminos de la vida.', artist: 'Los Diablitos' },
  { name: 'Ella era todo.', artist: 'Los Inquietos' },
  { name: 'No podran separarnos.', artist: 'Jorge Celedon' },
  { name: 'Muero por verla.', artist: 'Luis Mateus' },
  { name: 'Que me puedas amar.', artist: 'Miguel Morales' }
]

export default {
  name: 'app',
  data () {
    return {
      searchQuery: '',
      tracks: []
    }
  },
  /**
   * Computed Properties
   * Son funciones que devuelven un valor y dentro de estas funciones
   * puedo utilizar funciones ya existentes.
   */
  computed: {
    searchMessage () {
      return `Encontrados: ${this.tracks.length}`
    }
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
      this.tracks = tracks
    }
  }
}
</script>

<style lang="scss">
@import './scss/main.scss'
</style>
