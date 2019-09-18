<template>
    <div>
       <input v-model="frase"> <br>
       <span v-if="frase.length>0">Texto Original: <b>{{frase}}</b></span><br>
       <span v-if="frase.length>0">Texto Invertido: <b>{{invertir}}</b></span>
    </div>
</template>

<script>
export default {
    name: 'InvierteCadena',
    data() {
        return{
            frase: "Hola"
        }
    },
    computed:{
        invertir(){
            return this.frase.split('').reverse().join('').toUpperCase();
        }
    }
}
</script>