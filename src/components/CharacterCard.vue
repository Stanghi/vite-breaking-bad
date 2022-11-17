<script>
export default {
    name: 'CharacterCard',
    props: {
        character: Object,
    },
};
</script>

<template>
    <div class="calc-width">
        <div class="ms-card mb-5 text-center">
            <img :src="character.img" :alt="character.name" class="mb-3" />
            <h5>{{ character.name }}</h5>
            <p>{{ character.category }}</p>
            <p>{{ character.status }}</p>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/vars' as *;

.calc-width {
    width: calc(100% / 5);
}

.ms-card {
    height: 430px;
    width: 210px;
    padding: 15px;
    color: $text-card;
    background-color: $primary-color;

    img {
        width: 100%;
    }

    h5 {
        color: $text-white;
        font-weight: bold;
    }

    p {
        margin: 0;
    }
}
</style>
