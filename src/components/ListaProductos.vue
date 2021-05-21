<template>
  <div class="hello">
    <h1>Lista</h1>
    <ul id="example-1">
    <li v-for="(producto, index) in productos" :key="index">
        {{ index + 1 }} - Nombre: {{ producto.nombre }} - Precio: S/ {{ producto.precio }}
    </li>
</ul>
  </div>
</template>

<script>
export default {
  name: 'ListaProductos',
  props: ['productos']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
