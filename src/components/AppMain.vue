<template>
    <main class="pt-4">


        <!--*Drop down menù-->
        <div class="dropdown ms-5">
            <button class="btn btn-light dropdown-toggle" type="button" data-bs-toggle="dropdown" aria-expanded="false">
                Alien
            </button>
            <ul class="dropdown-menu">
                <li><button class="dropdown-item" type="button">Action</button></li>
                <li><button class="dropdown-item" type="button">Another action</button></li>
                <li><button class="dropdown-item" type="button">Something else here</button></li>
            </ul>
        </div>


        <CharacterList />
    </main>
</template>


<script>
import CharacterList from './CharacterList.vue';



export default {
    name: 'AppMain',
    data() {
        return {

        }
    },
    components: {
        CharacterList
    }
}
</script>


<style lang="scss"></style>