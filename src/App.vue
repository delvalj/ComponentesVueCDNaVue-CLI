<template>
  <div id="app" class="bg-success p-4 rounded-3">
    <h1 class="text-center p-2">DESAFIO III</h1>
    <h6 class="text-center p-1">Componentes Vue CDN a Vue CLI</h6>
    <component1 :array-prop="nuevoArray" :boolean-prop="boolean" :style-prop="estilo" class="text-center"></component1>
  </div>
</template>

<script>
import Component1 from "@/components/Component1";

export default {
  name: 'App',
  components: {
    Component1s
  },
  data() {
    return {
      nuevoArray: [
        {
          id: 0,
          nombre: 'Pepe',
          apellido: 'Sanchez',
          edad: 29,
        },
        {
          id: 1,
          nombre: 'Juanito',
          apellido: 'Makande',
          edad: 40,
        },
        {
          id: 2,
          nombre: 'Frank',
          apellido: 'Zappa',
          edad: 52,
        },
      ],

      boolean: true,
      estilo: 'background-color:red; font-family:Oswald; margin-top:25px;'
    }
  }

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  margin-top: 60px;
}
</style>
