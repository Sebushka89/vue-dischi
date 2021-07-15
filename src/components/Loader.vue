<template>
    <div class="loader">
        Loading...
    </div>
</template>

<script>

export default {
    name: 'Loader',
    
}
</script>

<style lang="scss" scoped>
.loader{
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    font-size: 30px;
}
</style>