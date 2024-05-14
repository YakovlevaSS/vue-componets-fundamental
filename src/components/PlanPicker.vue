<script setup>
import CoffeePlan from "./CoffeePlan.vue"
import {ref} from "vue"

const plans = ref(['The Addict', 'The Curious', 'The Single', 'The Hacke' ])
</script>

<template>
     <div class="plans">
    <CoffeePlan v-for="plan in plans" :key="plan" :name=plan></CoffeePlan>
  </div> 
</template>