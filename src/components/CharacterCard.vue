<template>
        <article class="card mb-3 col-2">
            <div class="px-0 mx-0">
                <img :src="image_url_small" class="card-img-top " alt="...">
            </div>
            <div class="card-body">
                <h5 class="card-title">
                    {{ name }}
                </h5>
                <p class="card-text">
                    {{ archetype }}
                </p>
            </div>
        </article>
</template>


<script>
export default {
    name: 'CharacterCard',
    data() {
        return {

        }
    },
    props:{
        name : String,
        archetype: String,
        image_url_small: String,
    }
}
</script>


<style lang="scss">
    .card-body{
        background-color: #D48F38;
    }
</style>