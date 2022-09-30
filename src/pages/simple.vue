<template>
    <div class="p-2">
      <h2>Page Simple</h2>
      <Card v-bind="unObjet0"/>
      <Card v-bind="unObjet1"/>
    </div>
   
</template>

<script setup lang="ts">
 import Card from '../components/card.vue';
 const props = defineProps({
  foo: String
});



const unObjet0 = {nom:"Villa France",
    prix: 5000000,
    favori: false,
    image: "./maison1.jpg", 
    nbrSDB: 6,}
const unObjet1 = {nom:"Villa Italie",
    prix: 400000,
    favori: false,
    image: "./maison2.jpg", 
    nbrSDB: 5,}

</script>


