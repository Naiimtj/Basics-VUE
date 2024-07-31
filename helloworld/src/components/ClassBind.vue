<template>
    <p :class="{ danger: hasError }"> <!-- v-bind y : es lo mismos / elemento: condición -->
            El Mensaje se ha enviado.
    </p>
    <p :style="{backgroundColor: '#ccc', color: c}"> 
        El Mensaje se ha enviado. 
    </p>
    <button @click="handleClick()">Cambiar Color</button>
</template>

<script lang="ts" setup>
    import {ref} from 'vue'
    let hasError = true;
    // Si no hay setup
    // import { defineComponent } from "vue";
    // export default defineComponent({
    //     name: 'ClassBind',
    //     setup() {
    //         let hasError = true;
    //         return { hasError };
    //     }
    // });
    let c = ref('#fff')
    const handleClick = () => {c.value = '#ff0000'}
</script>

<style>
    .danger {
    color: red;
    font-size: x-large
    }
</style>

