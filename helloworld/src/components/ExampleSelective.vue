<template>
       
    <h1 v-if="age < 18">ERES MENOR DE EDAD</h1>
    <h1 v-else>ERES MAYOR DE EDAD</h1>
    <!-- Cuando va cambiar muy a menudo mejora rendimiento-->
    <h1 v-show="age < 18">ERES MENOR DE EDAD</h1>
    <h1 v-show="age > 18">ERES MAYOR DE EDAD</h1>
</template>
<script lang="ts" setup>
    let age = 19
</script>

<!-- SIN SETUP (es lo mismo)
<script lang="ts">
    import {defineComponent} from 'vue'
    export default defineComponent({
    name: 'ExampleSelective',
    setup() {
        let age = 19
        return {age}
    }
    })
</script> 
-->

<style scoped>
    
</style>