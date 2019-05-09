<template>
    <div class="col-12">
        <p>Progress {{counter}}/10</p>
        <div class="progress" :style="{width: counter * 10 + '%'}"></div>
    </div>
</template>

<script>
export default {
    props: ['counter'],
}
</script>

<style>
.progress {
    background-color: orangered;
    height: 25px;
    width: 1%;
}
</style>
