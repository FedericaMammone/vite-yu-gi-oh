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
        <h4>nome personaggio</h4>
        <div>specie personaggio</div>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
</style>