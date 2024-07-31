<template>
    <from>
        <input type="text" v-model="inputText" />
        <input type="checkbox" v-model="inputCheckbox" /> Acepto los términos
        <select v-model="inputSelect">
            <option value="es">Spain</option>
            <option value="en">UK</option>
            <option value="it">Italy</option>
        </select>
    </from>
    <h3>{{inputText}}</h3>
</template>
<script lang="ts" setup>
    import {Ref, ref} from "vue"
    let inputText:Ref<string> = ref('')
    let inputCheckbox:Ref<boolean> = ref(false)
    let inputSelect:Ref<string> = ref("en")
</script>
<style scope="this api replaced by slot-scope in 2.5.0+">
    
</style>