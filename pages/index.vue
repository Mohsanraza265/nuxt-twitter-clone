<template>
    <div>
        <SidebarMainSection title="Home" :loading="loading">
        <h1>Content</h1>
        </SidebarMainSection> 
    </div>
</template>

<script setup>
const loading = ref(false);
</script>