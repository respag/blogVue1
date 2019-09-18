<template>
  <div>
    <div class="text-center">
      <img alt="frutas" src="@/assets/frutas.png" />
      <h2>Frutas</h2>
    </div>
    <b-alert variant="success" show>
      En esta vista creamos una lista de frutas a partir de un array definido en el almacén de <b>VUEX</b>.<br> 
      En la lista mostramos el nombre de la fruta y las cantidades de la misma, usando un componente <b>Badge de 
      Bootstrap</b>.<br>
      Al hacer click, sobre cada fruta, la cantidad se aumenta en una unidad.<br>
      En todo momento la lista se ordenará según las cantidades de mayor a menor.<br>
      Además, al hacer click en el botón <b>Reiniciar Lista</b>, las cantidades de todas las frutas
      se ponen en 0. 
    </b-alert>
    <ListaFrutas></ListaFrutas>
  </div>
</template>

<script>
import ListaFrutas from "@/components/ListaFrutas.vue";

export default {
  name: "frutas",
  components: {
    ListaFrutas
  }
};
</script>
