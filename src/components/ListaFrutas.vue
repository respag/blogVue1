<template>
  <div class="w-50 p-3">
    <ul class="list-group">
      <li
        v-for="(item, index) of frutasOrdenadas"
        :key="item.id"
        @click="aumentar(index)"
        class="list-group-item d-flex justify-content-between align-items-center"
      >
        {{item.nombre}}
        <span class="badge badge-primary badge-pill">{{item.cantidad}}</span>
      </li>
    </ul>
    <button class="btn btn-danger mt-5" @click="reiniciar">Reiniciar lista</button>
  </div>
</template>

<script>

import {mapState, mapMutations} from 'vuex';

export default {
    name: "listaFrutas",
    computed:{
      ...mapState(['frutas']),
      frutasOrdenadas(){
          return this.frutas.sort( (a,b)=>b.cantidad - a.cantidad)
      }
  },
  methods:{
      ...mapMutations(['aumentar', 'reiniciar'])
  }
};
</script>