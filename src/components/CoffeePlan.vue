<script setup>
const props = defineProps({
    name: {type: String, default: 'Default Plan'},
    price: {type: Number, required: true}
})
console.log(props.name)
</script>

<template>
        <div class="plan">
      <div class="description">
        <span class="title">{{ name }}</span>
      </div>
    </div>
</template>