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
    <div class="container">
        <div v-if="store.isLoaded" class="row">
            <div class="band-found-characters p-3 mb-4">Found {{ store.charactersListData.length }} characters</div>
            <CharacterCard v-for="(character, index) in store.charactersListData" :key="index" :character="character" />
        </div>
        <div v-else>
            <AppLoading />
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/vars' as *;

.container {
    background-color: $container-white;
    padding: 65px;
}

.band-found-characters {
    font-weight: bold;
    width: 100%;
    background-color: $band-found-characters;
}
</style>
