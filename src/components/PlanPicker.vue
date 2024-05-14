<script setup>
import CoffeePlan from "./CoffeePlan.vue"
import { ref } from "vue"

const plans = ref(['The Addict', 'The Curious', 'The Single', 'The Hacke'])
const selectedCoffeePlan = ref();

function handleSelectedCoffeePlan(name) {
    selectedCoffeePlan.value = name
}
</script>

<template>
    {{ selectedCoffeePlan }}
    <div class="plans">
        <CoffeePlan 
          v-for="plan in plans" 
          :key="plan" 
          :name=plan 
          :selected="plan ===selectedCoffeePlan"
          @selected="handleSelectedCoffeePlan"
          ></CoffeePlan>
    </div>
</template>