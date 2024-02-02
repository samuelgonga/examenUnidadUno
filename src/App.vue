<template>
  <div id="app">
    <header>
      <b-navbar type="dark" variant="dark">
        <b-navbar-nav>
          <b-nav-item href="#">Examen unidad 1</b-nav-item>
        </b-navbar-nav>
      </b-navbar>
    </header>

    <main>
      <div class="col-10">
            <b-col>
              <router-view></router-view>
            </b-col>   
          </div>
      <!-- <div>
        <b-container>
            <b-breadcrumb :items="items"></b-breadcrumb>
        </b-container>          
        <h1 class="text-center">Inicio</h1>         
        <div class="mt-2">          
          <b-button variant="outline-success" :to="{ name: 'formulario'}">Formulario</b-button>  
        </div>             
        <div class="mt-2">
          <b-button variant="outline-danger" :to="{ name: 'paginacion'}" >Paginacion</b-button>               
        </div> 
    </div>     -->
      <TheWelcome />
    </main>
  </div>
  
</template>

<script>
export default {
    data() {
      return {
        items: [
          {
            text: 'Inicio',
            href: '#'
          },
        ]
      }
    }
  }
</script>

<style>

</style>