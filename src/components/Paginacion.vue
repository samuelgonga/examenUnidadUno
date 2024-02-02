<template>
    <div>
        <b-container>
            <b-breadcrumb :items="items"></b-breadcrumb>
        </b-container>        
        <h1>Paginacion</h1>
        <div class="overflow-auto">
    <b-pagination
      v-model="currentPage"
      :total-rows="rows"
      :per-page="perPage"
      aria-controls="my-table"
    ></b-pagination>

    <p class="mt-3">Current Page: {{ currentPage }}</p>

    <b-table
      id="my-table"
      :items="items"
      :per-page="perPage"
      :current-page="currentPage"
      small
    ></b-table>
  </div>
    </div>
</template>

<script>
export default {
    data(){
        return {
        items: [
        {
            text: 'Inicio',
            to: { name: 'inicio' }
          },
          {
            text: 'paginacion',
            active: true
          },                    
        ],
    }
}
}
</script>

<style>

</style>