<script setup>
defineProps({
    id: {
        type: String,
        required: true,
    },
});
</script>

<template>
    <p>{{ id }}</p>
</template>
