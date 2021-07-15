<template>
    <div class="bg-fluid">

        <div class="container">

            <div class="row">

                <Discs class="custom-col" v-for="(disc, index) in discs" :key="index"
                :poster="disc.poster"
                :title="disc.title"
                :author="disc.author"
                :genre="disc.genre"
                :year="disc.year"
                :inputSearch="inputSearch" />
                    
            </div>
        </div>
    </div>
</template>

<script>

import Discs from './Discs.vue';

export default {
    name: 'Main',
    components: {
        Discs
    },
    props: {
        discs: Array,
        inputSearch: String
    }
    
}
</script>

<style lang="scss" scoped>
.bg-fluid {
        background-color: rgb(30,45,59);
        padding-top: 25px;
        height: 100vh;
        .container {
            .row {
                .custom-col {
                    width: calc( 100% / 5)
                }
            }
        }
    }
</style>