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
            <SingleCharacter v-for="character in store.characterList" :details="character" />
        </section>
    </main>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;

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
    }
}
</style>