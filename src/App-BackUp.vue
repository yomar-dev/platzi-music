<template lang="pug">
  #app
    p(v-show="showValue") {{ value }}
    p(v-if="showValue") {{ value }}
      span Mensaje
    p(v-else) {{ 'Hola Mundo!!' }}

    ul
      li(v-for="i in items") {{ i }}


    a(v-bind:href="url" target="_blank") Link
    br

    input(v-model="name" placeholder="Ingresa tu nombre")
    input(v-model="lastName" placeholder="Ingresa tu apellido")
    p {{ fullName }}

    <!-- La directiva 'v-on' recibe el tipo de evento que queremos enlazar sobre este elemento, en este caso es el evento 'click' y recibe como valor el nombre del metodo, en este caso el metodo 'format'. Algo a tener en cuenta es que podemos remplazar 'v-on' por '@' y obtendremos el mismo resultado. -->
    button(v-on:click="format") Format
    p {{ formattedName }}
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
      name: '',
      url: 'https://platzi.com/@yomar_dev/',
      lastName: '',
      formattedName: ''
    }
  },
  /**
   * Computed Properties
   * Son funciones que devuelven un valor y dentro de estas funciones
   * puedo utilizar funciones ya existentes.
   */
  computed: {
    fullName () {
      //return this.name + ' ' + this.lastName
      return `${this.name} ${this.lastName}`
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
    /**
     * Los watchers reciben el valor nuevo y el viejo de la propiedad.
     */
    name (newVal, oldVal) {
      console.log(newVal, oldVal)
    }
  },
  methods: {
    format () {
      this.formattedName = this.name.split(' ').join('-').toUpperCase()
    }
  }
}
</script>

<style lang="scss">
@import './scss/main.scss'
</style>
