<template>
    <div>
        <header>
            <img src="../assets/spotify-logo.png" alt="">
            <div class="ricerca">
                <input type="text" placeholder="Cerca per canzone, artista o anno" v-model="searchString" @keyup.enter="$emit('search', searchString)" />
                <button class="pulsante" @click="$emit('search', searchString)">Cerca</button>
            </div>
        </header>
    </div>
</template>

<script>

export default {
    name: 'Header',
    data() {
        return {
            searchString: '',
        }
    }, 

}
</script>

<style lang="scss" scoped>
    header{
        background-color: rgb(46,58,70);
        display: flex;
            justify-content: space-between;
            align-items: center;

        img{
            width: 50px;
            margin: 10px 0;
        }
        .ricerca{
            input{
                width: 300px;
            }
            .pulsante{
                margin-right: 20px;
                border: 1px solid white;
                width: 80px;background-color: white;
                border-left: transparent;
                border-top-right-radius: 25px;
                border-bottom-right-radius: 25px;
                font-weight: bold;
            }
        }
    }
</style>