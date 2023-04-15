 <!-- <template>
    <div>
      <b-form-select v-model="selected" :categorias="categorias" multiple>
        <template #first>
          <b-form-select-option :value="null" disabled>Seleccione una o varias opciones</b-form-select-option>
        </template>
        <b-form-select-option v-for="option in categorias" :key="option.id" :value="option.url">{{ option.nombre }}</b-form-select-option>
      </b-form-select>
      <div class="mt-3">Selected: <strong>{{ selected }}</strong></div>
    </div> 
    <b-form-group  v-slot="{ ariaDescribedby }">
      <b-form-checkbox-group 
        id="checkbox-group-1"
        v-model="selected"
        :options="options"
        :aria-describedby="ariaDescribedby"
        name="flavour-1"
      ></b-form-checkbox-group>
      <div class="mt-3">Selected: <strong>{{ selected }}</strong></div>
    </b-form-group>
  </template> 
  <template>
    <div>
      <b-form-checkbox-group v-model="selectedItems" :options="apiResults"></b-form-checkbox-group>
      <b-button @click="fetchApiData()">Cargar resultados</b-button>
    </div>
  </template>
  

<script>


  export default {
    data() {
      return {
        selected: ['b'], // Array reference
        categorias: null,
        options: [
          { value: 'a', text: 'This is First option' },
          { value: 'b', text: 'Default Selected Option' },
          { value: 'c', text: 'This is another option' },
          { value: 'd', text: 'This one is disabled', disabled: true },
          { value: 'e', text: 'This is option e' },
          { value: 'f', text: 'This is option f' },
          { value: 'g', text: 'This is option g' }
        ]
      } 
    },
    methods:{
        async getCategoria(){
            await this.axios('http://127.0.0.1:8000/api/categoria/').then(response=>{
                this.categorias = response.data
            })
        }
    },
    async mounted(){
        await this.getCategoria()
    }
  }
</script> -->
<template>
    <div>
      <b-form-checkbox-group v-model="selectedItems" :options="apiR 
      esults"></b-form-checkbox-group>
      <b-button @click="fetchApiData()">Cargar resultados</b-button>
    </div>
  </template>
<script>
export default{
    data() {
    return {
        selectedItems: [],
        apiResults: []
  }
}

}
</script>