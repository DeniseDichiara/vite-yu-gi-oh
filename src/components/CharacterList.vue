<template>
    <div>
        <h2>
            CharacterList
        </h2>
        <CharacterCard />
    </div>
</template>


<script>
import CharacterCard from './CharacterCard.vue';

export default {
    name: 'CharacterList',
    data(){
        return {

        }
    },
    components: {
        CharacterCard
    }
}
</script>


<style lang="scss">
    
</style>