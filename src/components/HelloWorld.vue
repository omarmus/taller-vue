<template>
  <div class="hello">
    <h1>{{ numero }}</h1>
    <input type="text" v-model="numero">
    <h3 v-if="lista.length == 0">No hay elementos</h3>
    <ul v-else>
      <li>Lista</li>
      <li v-for="item in lista">{{ item }}</li>
    </ul>
    <button @click="agregar">Agregar numero</button>
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
      let suma = 0;
      for (let i in this.lista) {
        suma += parseInt(this.lista[i])
      }
      alert(suma)
    }
  }
}
</script>
