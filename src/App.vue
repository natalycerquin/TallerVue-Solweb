<template>
  <div id="app" class="container">
    <img alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld msg="Soluciones web - Registrador de productos" />
    <div class="row">
      <div class="col-4">
        <Formulario v-on:on-guardar="agregarProducto" />
      </div>
      <div class="col-6">
        <ListaProductos v-bind:productos="productos" />
      </div>
    </div>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Formulario from "./components/Formulario";
import ListaProductos from "./components/ListaProductos";

export default {
  name: "App",
  components: {
    HelloWorld,
    Formulario,
    ListaProductos,
  },
  data: function () {
    return {
      productos: [],
    };
  },
  methods: {
    agregarProducto(nombre, precio) {
      const producto = { nombre: nombre, precio: precio };
      this.productos.push(producto);
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
