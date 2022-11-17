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
    <div v-if="store.isLoaded" class="container p-5">
        <div class="row">
            <CharacterCard />
        </div>
    </div>
    <div v-else>
        <AppLoading />
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/vars' as *;

.container {
    background-color: $container-white;
}
</style>
