<script setup>
import { ref } from 'vue';

const modelValue = defineModel();
const isFocused = ref(false);

const handleInput = (event) => {
    event.preventDefault();

    if (/^[1-9]$/.test(event.key)) {
        modelValue.value = event.key;
    } else if (
        event.key === 'Escape' ||
        event.key === 'Backspace' ||
        event.key === 'Delete'
    ) {
        modelValue.value = '';
    }
};
</script>

<template>
    <div
        class="flex justify-center items-center w-17 h-17 border border-gray-300 rounded"
        :class="{ 'bg-blue-100 border-blue-400': isFocused }"
    >
        <input
            type="text"
            v-model="modelValue"
            @keydown="handleInput"
            @focus="isFocused = true"
            @blur="isFocused = false"
            class="w-15 h-15 text-center text-6xl font-semibold bg-transparent border-none caret-transparent focus:outline-none cursor-default"
        />
    </div>
</template>
