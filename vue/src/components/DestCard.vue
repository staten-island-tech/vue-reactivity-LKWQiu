<template>
    <div>
        <h1>{{ Destination.name }}</h1>
        <img :src="Destination.img" alt="">
    </div>
</template>

<script setup>
    const props = defineProps({
        Destination: Object,
    });
</script>