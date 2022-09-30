<script setup lang="ts">
    import {ref} from "@vue/reactivity";
import Card from "./card.vue";
    const submitted = ref(false)
        const submitHandler = async () => {
        await new Promise((r) => setTimeout(r, 1000))
        submitted.value = true
}
    
    const maison = ref({});
    </script>

    <template>
        <div>
            <div class="p-2">
                <h2 class="text-2xl"> Résultats </h2>
                <Card v-bind="maison" />
                <FormKit type="form"  
                        v-model="maison"
                        :config="{ 
                            classes: {
                                input: 'p-1 rounded border-gray-300 shadow-sm border',
                                label: 'text-gray-600',
                            },
                        }"
                        :submit-attrs="{ classes: { input: 'bg-red-300 p-1 rounded' } }">
                    <FormKit name="nom" label="nom" />
                    <FormKit name="prix" label="prix" type="number" />
                    <FormKit name="favori" label="mettre en valeur"  type="checkbox" wrapper-class="flex" />
                   
                </FormKit>
            </div>
        </div>
        
    </template>

