<template>
  <ul>
    <h1>Lista</h1>
    <label>Tarea </label>
    <input type="text" v-model="input" placeholder="Ingresa una nueva Tarea" style="width: 250px" />
    <button class="btn btn-secondary" @click="agregarPersona">Agregar</button>
    <h2>Crear una Lista</h2>
    <li v-for="(item, index) in items" :key="index">{{ index }} {{ item }}</li>
  </ul>
</template>
<script>
export default {
  name: 'app',
  data: function () {
    return {
      input: '',
      items: [],
    }
  },

  methods: {
    agregarPersona() {
      if (!this.input) {
        return
      }
      this.items.push(this.input)

      this.input = ''
    },
  },
}
</script>
