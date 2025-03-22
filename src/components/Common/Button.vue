<script setup>
import { defineProps, ref } from 'vue';

const props = defineProps({
    text: {
        type: String,
        required: true,
    },

    color: {
        type: String,
        required: false,
        default: 'white',
    },
});

const backgroundColorClass = ref('bg-white');
const backgroundHoverColorClass = ref('hover:bg-gray-50');

if (props.color === 'blue') {
    backgroundColorClass.value = 'bg-blue-500';
    backgroundHoverColorClass.value = 'hover:bg-blue-600';
}
</script>

<template>
    <button class="btn btn-soft btn-primary" text="">{{ props.text }}</button>
</template>
