<script setup>
import Logo from '@/components/Logo.vue';
</script>

<template>
    <footer
        class="footer sm:footer-horizontal footer-center bg-neutral text-neutral-content items-center p-4"
    >
        <aside class="grid-flow-col items-center">
            <Logo />
            <p>
                Copyright © {{ new Date().getFullYear() }} - All right reserved
            </p>
        </aside>
    </footer>
</template>
