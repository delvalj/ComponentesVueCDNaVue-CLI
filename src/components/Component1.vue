<template>
  <div class="container">
  <table v-if="arrayProp.length" :style="styleProp" class="table p-3 rounded-3">

    <tr class="bg-danger">
      <th>ID</th>
      <th>NOMBRE</th>
      <th>APELLIDO</th>
      <th>EDAD</th>
      <th>BOOLEAN</th>
    </tr>

    <tr v-for="persona in arrayProp" :key="persona.id">
      <td>
        {{ persona.id }}
      </td>

      <td>
        {{ persona.nombre }}
      </td>

      <td>
        {{ persona.apellido }}
      </td>

      <td>
        {{ persona.edad }}
      </td>

      <td>
        {{ booleanProp }}
      </td>


    </tr>
  </table>
  </div>
</template>


<script>

export default {
  name: "Component1",
  props: {
    arrayProp: {
      type: Array,
      default: () => []
    },
    booleanProp: {
      type: Boolean,
      default: null
    },
    styleProp: {
      type: String,
      default: ''
    }
  },
}
</script>

<style scoped>

</style>