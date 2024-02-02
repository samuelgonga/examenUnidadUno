<template>
    <div>
        <b-container>
            <b-breadcrumb :items="items"></b-breadcrumb>
        </b-container>       
        <h1>Inicio</h1>
        <b-container>
          <b-button variant="outline-success" :to="{ name: 'formulario'}">Formulario</b-button>
        </b-container>
        <b-container>
          <b-button variant="outline-success" :to="{ name: 'paginacion'}">Paginacion</b-button>
        </b-container>
    </div>
</template>

<script>
export default {
    data() {
      return {
        items: [
          {
            text: 'inicio',
            active: true
          }
        ]
      }
    }
  }
</script>

<style>

</style>