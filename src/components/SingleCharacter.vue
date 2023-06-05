<script>
export default {
    name: 'SingleCharacter',
    props: {
        details: Object
    }
}

</script>

<template>
    <div class="character text-center">
        <img :src="details.card_images[0].image_url_small" alt="info.image">
        <h5> {{ details.name }}</h5>
        <span class="specie">{{ details.race }}</span>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;

.character {
    .specie {
        color: white;
    }
}
</style>