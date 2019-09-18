<template>
  <div>
   <h2>Generalidades</h2>
   <p>
     Esta es la vista inicial. En la misma usamos un componente <b>InvierteCadena</b>
     que permite que el usuario escriba una cadena de texto y la devuelve invertida y en mayúsculas.
   </p>
   <InvierteCadena></InvierteCadena>
  </div>
</template>

<script>
// @ is an alias to /src
import InvierteCadena from '@/components/InvierteCadena.vue'

export default {
  name: 'home',
  components: {
    InvierteCadena
  }
}
</script>
