<script setup>

const props = defineProps({
    name: { type: String, default: 'Default Plan', validator(value){
        return value.startsWith("The") ? true :false
    } },
    selected: {type: Boolean, default: false}
    // price: { type: Number, required: true }
})
const emit = defineEmits({
    selected(payload) {
        return typeof payload ==='string'
    }
})

function selectPlane() {
    emit('selected', props.name)
}
</script>

<template>
    <div @click="selectPlane" class="plan" :class="{ 'active-class': selected }">
        <div class="description">
            <span class="title">{{ name }}</span>
        </div>
    </div>
</template>

<style scoped>
.active-class {
    color: coral;
}
</style>