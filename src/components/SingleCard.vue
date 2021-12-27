<template>
    <div class="card">
        <div class="card_img text-center">
            <img :src="myprops.image" :alt="myprops.name">
        </div>
        <div class="card_title text-center">
            <h2>{{myprops.name}}</h2>
        </div>

        <div class="card_origin text-center">{{myprops.origin}}</div>
        <div class="card_species text-center">{{myprops.species}}</div>

    </div>
</template>

<script>
export default {
    name:'SingleCard',
    props:{
        myprops:Object,
    },
}
</script>

<style lang="scss" scoped>
@import '../style/variables';

.card{
    min-width: 300px;
    max-width: 300px;
    padding: 10px;
    margin-bottom: 50px;

    &_img{        
        margin: auto;
        max-width: 200px;
        overflow: hidden;
        img{
        border-radius: 50%;

        }

    }

    &_title{
        margin: 10px 0;
        h2{
            color:$brand_subtitles;
        }

        &::after{
            content:"";
            width:40px;
            height: 3px;
            background-color:black;
            display: block;
            margin: 20px auto;
        }
    }
    &_species{
        font-weight: bold;
    }
}



</style>