<template>
    <div>
        <b-container>
            <b-breadcrumb :items="items"></b-breadcrumb>
        </b-container>        
        <h1>Formulario de vehiculo</h1>

        <div>
    <b-form @submit="onSubmit" @reset="onReset" v-if="show">
      <b-form-group
        id="input-group-1"
        label="Marca:"
        label-for="input-1"
      >
        <b-form-input
          id="input-1"
          v-model="form.marca"
          type="text"
          placeholder="Ingresa la marca de tu vehiculo"
          required
        ></b-form-input>
      </b-form-group>
      <hr>
      <b-form-group id="input-group-2" label="Modelo:" label-for="input-2">
        <b-form-input
          id="input-2"
          type="number"
          v-model="form.modelo"
          placeholder="Ingresa el modelo de tu vehiculo"
          required
        ></b-form-input>
      </b-form-group>
      <hr>
      <b-form-group id="input-group-3" label="Año de fabricacion:" label-for="input-3">
        <b-form-input
          id="input-3"
          v-model="form.anioFabricacion"
          placeholder="Ingresa el año de fabricacion"
          required
        ></b-form-input>
        <hr>
        
      </b-form-group>
      <b-form-group id="input-group-4" label="Numero de serie:" label-for="input-4">
        <b-form-input
          id="input-4"
          v-model="form.numSerie"
          placeholder="Ingresa el numero de serie"
          required
        ></b-form-input>
      </b-form-group>    
      <hr>
      

      <b-button type="submit" variant="primary">Submit</b-button>
      <b-button type="reset" variant="danger">Reset</b-button>
    </b-form>
    <b-card class="mt-3" header="Form Data Result">
      <pre class="m-0">{{ form }}</pre>
    </b-card>
  </div>
    </div>
</template>

<script>
export default {
    data() {
      return {
        items: [
        {
            text: 'Inicio',
            to: { name: 'inicio' }
          },
          {
            text: 'formulario',
            active: true
          },          
        ],
        form: {
          marca:'',
          modelo:'',
          anioFabricacion:'',
          numSerie:'',
        },
        show: true
      }
    },
    methods: {
      onSubmit(event) {
        event.preventDefault()
        alert(JSON.stringify(this.form))
      },
      onReset(event) {
        event.preventDefault()
        // Reset our form values
        this.form.marca = ''
        this.form.modelo = ''
        this.form.anioFabricacion = ''
        this.form.numSerie = ''
        // Trick to reset/clear native browser form validation state
        this.show = false
        this.$nextTick(() => {
          this.show = true
        })
      }
    }
  }
</script>

<style>

</style>