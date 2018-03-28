<template>
  <div class="hello">
    <h1>Número: {{ numero }}</h1>
    Ingrese un número <input type="text" v-model="numero">
    <h3 v-if="lista.length == 0">No hay elementos</h3>
    <ul v-else>
      <li>Lista de números</li>
      <li v-for="item in lista" :key="item">{{ item }}</li>
    </ul>
    <button @click="agregar">Agregar número</button>
    <button @click="sumar">Sumar todo</button>
  </div>
</template>

<script>
export default {
  data () {
    return {
      numero: '',
      lista: []
    }
  },
  methods: {
    agregar () {
      let numero = this.numero
      this.lista.push(numero)
    },
    sumar () {
      let suma = 0
      for (let i in this.lista) {
        suma += parseInt(this.lista[i])
      }
      alert(suma)
    }
  }
}
</script>
