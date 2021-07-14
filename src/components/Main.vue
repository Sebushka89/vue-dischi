<template>
    <div>
        <Discs v-for="(disc, index) in discs" :key=index
        :poster='discs.poster'
        :title='discs.title'
        :author='discs.author'
        :genre='discs.genre'
        :year='discs.year' />
    </div>
</template>

<script>

import Discs from './Discs.vue'

export default {
    name: 'Main',
    components: {
        Discs
    },
    props: {
        discs: Array
    }
    
}
</script>

<style lang="scss" scoped>

</style>