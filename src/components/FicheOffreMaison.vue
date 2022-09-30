<script setup lang="ts">
    import Card from "../components/card.vue";
      const res = await fetch("/maisons-public.json")
      const maisons =  await res.json()
       
     console.log(maisons);
     
     
     </script>
     <template>
        <div class="p-2">     
             <Card
           v-for="maison in maisons"
           :key="maison.nom"
           v-bind="maison"/>
           </div>

       
    </template>