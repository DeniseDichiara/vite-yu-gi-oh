<template>
    <div class="container">
        <div class="row p-5 justify-content-between">
            <div class="col-12 my_found-cards d-flex align-items-center mt-2">
                <p>
                    Found 39 cards
                </p>
            </div>
            <CharacterCard v-for="character in charactersList" 
                :name="character.name"
                :archetype="character.archetype"
                :image="character.card_images[0].image_url_small"
            />
        </div>
    </div>
</template>


<script>
import CharacterCard from './CharacterCard.vue';
import axios from 'axios';

export default {
    name: 'CharacterList',
    data() {
        return {
            charactersList : [],
        }
    },
    components: {
        CharacterCard
    },

    created() {

        axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
            .then( (response) => {
                console.log(response.data.data);
                this.charactersList = response.data.data;
            })
            .catch(function (error) {
                console.log(error);
            })
    }
}
</script>


<style lang="scss" scoped>
    .container{
        background-color: white;
        .my_found-cards{
            background-color: black;
            color: white;
        }
    }
</style>