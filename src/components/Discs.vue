<template>
   <div class="disc-container">
        <div class="disc-content">
            <img :src="poster" alt="">
            <h3>{{ title }}</h3>
            <div class="info">{{ author }}</div>  
            <div class="info">{{ year}}</div>     
        </div>
    </div>
</template>

<script>
export default {
    name: 'Discs' ,
    props:{
       poster: String,
       title: String,
       author: String,
       genre: String,
       year: String
    }

}
</script>

<style lang="scss" scoped>
.disc-container {
        text-align: center;
        .disc-content {
            margin: 15px 10px;
            background-color: rgb(46, 58, 70);
            padding: 20px;
            height: 400px;
            img {
                width: 100%;
            }
            h3 {
                text-transform: uppercase;
                padding: 15px 0;
                color: white;
                font-size: 24px;
            }
            div.info {
                color: #888;
                font-weight: bolder;
            }
        }
    }

</style>