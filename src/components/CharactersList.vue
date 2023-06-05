<script>
import { store } from './../store';

import SingleCharacter from './SingleCharacter.vue'

export default {
    name: 'CharactersList',
    components: {
        SingleCharacter
    },
    data() {
        return {
            store,
        }
    }
}

</script>

<template>
    <main>

        <select name="Category" id="">
            <option value="Alien">Alien</option>
            <option value="Monster">Monster</option>
            <option value="MonsterAlien">MonsterAlien</option>
        </select>

        <section class="container">
            <div class="risultato">
                <span>
                    <strong>Found 39 cards</strong>
                </span>
            </div>
            <div class="row">
                <div v-for="character in store.characterList" :key="character.id" class="carta">

                    <SingleCharacter :details="character" />
                </div>
            </div>

        </section>
    </main>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;

main {

    height: 100%;

    select {
        padding: 5px;
        border: 0;
        border-radius: 5px;
        margin-top: 20px;
        margin-left: 10%;
    }

    .container {

        width: 85%;
        height: 80%;
        background-color: $secondary;
        margin: 20px auto;
        padding: 25px;

        .risultato {
            @include center(horizontal);
            width: 100%;
            height: 50px;
            background-color: black;
            margin: 0;
            color: white;
        }

        .row {}

        .carta {
            width: calc((100% / 5) - 20px);
            background-color: $primary;
            margin: 0px 10px 10px 10px;

        }
    }
}
</style>