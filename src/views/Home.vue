<script setup>
import SudokuBoard from '@/components/SudokuBoard/SudokuBoard.vue';
import Toolbar from '@/components/Toolbar/Toolbar.vue';
</script>

<template>
    <div class="flex flex-col items-center gap-5">
        <Toolbar />
        <SudokuBoard />
    </div>
</template>
