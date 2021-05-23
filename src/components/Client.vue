<template>
    <div class="client">
        <img
            :src="`/images/${imageFileName}`"
            :alt="altText"
        >
    </div>
</template>

<script>
    export default {
        props: {
            imageFileName: {
                type: String,
                required: true,
            },
            altText: {
                type: String,
                required: true,
            }
        },
    }
</script>