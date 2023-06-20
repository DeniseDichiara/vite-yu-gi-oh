<template>
    <div class="container">
        <div class="row p-5">
            <CharacterCard />
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

        }
    },
    components: {
        CharacterCard
    },

    //**Chiamata API, mi serve AXIOS */
    created() {

        axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
            .then(function (response) {
                // handle success
                console.log(response);
            })
            .catch(function (error) {
                // handle error
                console.log(error);
            })
    }
}
</script>


<style lang="scss">
main {
    background-color: orange;
}
</style>