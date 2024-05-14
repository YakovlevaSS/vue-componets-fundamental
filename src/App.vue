<script setup>
import PlanPicker from "./components/PlanPicker.vue"
import FansyButton from "./components/FansyButton.vue"
</script>

<template>
  <h2 class="subtitle">
    We travel the world
  </h2>

<PlanPicker/>

<FansyButton>
<template #icon="{hover}">
  !! {{ hover ? 'hi' : 'by'}}
</template>
submit
</FansyButton>

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
