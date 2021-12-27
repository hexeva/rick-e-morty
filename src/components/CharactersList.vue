<template>
<div class="row row-cols-2 row-cols-lg-4">
    <div class="cards_collection">
        <SingleCard v-for=" character in arrayCards" :key="character.id" :myprops="character" />
        

    </div>


</div>

</template>

<script>
import axios from "axios";

import SingleCard from "./SingleCard.vue"

export default {
    name:'CharactersList',
    components:{
        SingleCard,
    },

    data:function(){
        return{
            arrayCards:[],
        };
    },

    created:function(){
        axios.get('https://api.sampleapis.com/rickandmorty/characters')
        .then ((response) => {
            // console.log(response.data);
            this.arrayCards = response.data;
        });
    },
}
</script>

<style lang="scss" scoped>

.cards_collection{
    width: 100%;
    padding: 30px 0;
    display: flex;
    flex-wrap:wrap;
    
}

</style>