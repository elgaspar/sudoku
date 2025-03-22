<script setup>
import Footer from '@/components/Footer.vue';
import Logo from '@/components/Logo.vue';
</script>

<template>
    <div class="flex flex-col min-h-screen">
        <header>
            <div class="navbar bg-neutral text-neutral-content gap-3">
                <Logo />
                <a class="text-xl font-bold" href="/">Sudoku</a>
            </div>
        </header>

        <main class="bg-base-100 py-5 flex-1">
            <div class="mx-auto max-w-7xl">
                <div class="rounded-lg bg-white p-6 shadow-sm">
                    <slot></slot>
                </div>
            </div>
        </main>

        <Footer />
    </div>
</template>
