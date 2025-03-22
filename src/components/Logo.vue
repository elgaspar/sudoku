<script setup>
import { defineProps } from 'vue';

const props = defineProps({
    size: {
        type: Number,
        required: false,
        default: 32,
    },
});
</script>

<template>
    <!--    TODO: change image-->
    <img src="/logo.svg" alt="Logo" :style="{ width: props.size + 'px' }" />
</template>
