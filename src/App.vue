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
      lastName: ''
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
  }
}
</script>

<style lang="scss">
@import './scss/main.scss'
</style>
