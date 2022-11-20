<script>
import axios from 'axios';
import { store } from './data/store';

import AppHeader from './components/AppHeader.vue';
import CategorySelect from './components/CategorySelect.vue';
import CharacterList from './components/CharacterList.vue';

export default {
    name: 'App',
    data() {
        return {
            store,
        };
    },
    components: {
        AppHeader,
        CategorySelect,
        CharacterList,
    },
    methods: {
        getCharachers() {
            store.isLoaded = false;
            axios
                .get(store.apiUrl, {
                    params: { category: store.filterWhitValue },
                })
                .then((result) => {
                    store.charactersListData = result.data;
                    store.isLoaded = true;
                })
                .catch((error) => {
                    console.log('error', error);
                });
        },
    },
    mounted() {
        this.getCharachers();
    },
};
</script>

<template>
    <AppHeader title="Breaking Bad Api" />
    <main>
        <CategorySelect @changeFilter="$emit(getCharachers())" />
        <CharacterList />
    </main>
</template>

<style lang="scss">
@use './styles/general';
</style>
