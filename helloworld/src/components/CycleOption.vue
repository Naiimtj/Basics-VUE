<template>
    <div>Hola Mundo</div>
</template >

<script lang="ts" setup>
import { onMounted, onUpdated } from 'vue';

onMounted(() => {
    console.log("Mounted");    
})

onUpdated(() => {
    console.log("Update");    
})

</script>

<style scoped>
</style>

<!-- export default defineComponent({
    name: "CycleOption",
    methods: {},
    created() {
        console.log("Created");        
    },
    mounted() {
        console.log("Mounted");
    },
    updated() {
        console.log("Update");
    },
    unmounted() {
        console.log("UnMounted");        
    },
}) -->