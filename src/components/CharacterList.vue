<script>
import { store } from '../data/store';
import CharacterCard from './CharacterCard.vue';
import AppLoading from './AppLoading.vue';

export default {
    name: 'CharacterList',
    components: {
        AppLoading,
        CharacterCard,
    },
    data() {
        return {
            store,
        };
    },
};
</script>

<template>
    <p>CharacterList</p>
</template>

<style lang="scss" scoped></style>
