<template>
    <div class="p-2">
      <h2>Page Liste</h2>
      <Card v-for="unObjet of desObjets" v-bind="unObjet" :key="unObjet.nom"/>
    </div>
  
</template>

<script setup lang="ts">
 import Card from '../components/card.vue';
 const props = defineProps({
  foo: String
});



const desObjets = [{nom:"Villa France",
    prix: 500000,
    favori: false,
    image: "./maison1.jpg", 
    nbrSDB: 6,},
    
  {nom:"Villa Italie",
    prix: 400000,
    favori: false,
    image: "./maison2.jpg", 
    nbrSDB: 5,},
];

</script>


