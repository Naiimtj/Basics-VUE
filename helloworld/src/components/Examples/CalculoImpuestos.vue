<template>
  <div>
    <label v-custom-font.red>Subtotal</label>
    <input type="number" v-model="subtotal" />
    <h3 v-custom-font.xl.blue>Total Impuestos a Pagar {{ totalVat }} ({{ vat }}%)</h3>
  </div>
</template>

<script lang="ts" setup>
import { computed, ref, Ref } from 'vue';

const vat = 21
let subtotal :Ref<number> = ref(0)
const totalVat = computed(() => (vat*subtotal.value)/100)
</script>

<style scoped></style>
