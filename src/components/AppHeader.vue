<script >

export default {
    name: 'AppHeader',
}
</script>

<template>
    <header>
        <div class="logo">
            <img src="https://ygoprodeck.com/cdn-cgi/image/width=150/https://images.ygoprodeck.com/assets/images/ygoprodeck_logo.png"
                alt="Logo">
        </div>

        <div class="title">
            <h1>Yu-Gi-Oh Api</h1>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins.scss' as *;
@use '../styles/partials/variables.scss' as *;

header {
    @include center('horizontal');

    height: 100px;
    background-color: $secondary;

    .logo img {
        height: 40px;
    }
}
</style>
