<template>
    <div class="col-12 preview">
        {{preview}}
    </div>
</template>

<script>
export default {
    props: ['preview'],
}
</script>

<style scoped>
    .preview {
        font-family: "Arizonia";
        font-size: 3em;
    }
</style>
