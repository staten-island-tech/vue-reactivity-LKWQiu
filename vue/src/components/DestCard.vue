<template>
    <div class="card">
        <h1>{{ Destination.name }}</h1>
        <img class="img" :src="Destination.img" alt="">
    </div>
</template>

<script setup>
    const props = defineProps({
        Destination: Object,
    });
</script>

<style scoped>
.card{
    width: 50%;
    height: 50%;
}
.img{
    width: inherit;
    object-fit: contain;
}
</style>