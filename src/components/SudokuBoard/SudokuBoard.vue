<script setup lang="ts">
import { ref, watch, computed } from 'vue';
import Input from '@/components/SudokuBoard/Input.vue';

const cells = ref(
    Array(81)
        .fill()
        .map(() => ({
            value: null,
        })),
);

watch(
    cells,
    (newCells) => {
        //TODO
        console.log('ok');
        // console.table(newCells);
    },
    { deep: true },
);
</script>

<template>
    <div class="grid grid-cols-9 gap-1 w-fit">
        <Input
            v-for="(cell, index) in cells"
            :key="index"
            v-model="cell.value"
        />
    </div>
</template>
