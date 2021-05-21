<template>
  <div>
    <h1>Formulario</h1>
    <div class="form-group mt-3">
      <label for="">Nombre</label>
      <input type="text" class="form-control" v-model="nombre" />
      <p>Nombre es: {{ nombre }}</p>
    </div>
    <div class="form-group mt-3">
      <label for="">Precio</label>
      <input type="number" class="form-control" v-model="precio" />
      <p>El precio es: {{ precio }}</p>
    </div>
    <button class="btn btn-primary w-100" v-on:click="guardarProducto()">
      Guardar
    </button>
  </div>
</template>

<script>
export default {
  name: "Formulario",
  data: () => {
    return {
      nombre: "",
      precio: 0,
    };
  },
  methods: {
    guardarProducto: function () {
      const nombre = this.nombre;
      const precio = this.precio;
      this.$emit("on-guardar", nombre, precio);
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
