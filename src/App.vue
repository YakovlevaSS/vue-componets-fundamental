<script setup>
import CoffeePlan from "./components/CoffeePlan.vue"
import {ref} from "vue"

const plans = ref(['The Addict', 'The Curious', 'The Single', 'The Hacke' ])
</script>

<template>
  <h2 class="subtitle">
    We travel the world
  </h2>

  <div class="plans">
    <CoffeePlan v-for="plan in plans" :key="plan" :name=plan></CoffeePlan>
  </div>

</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
