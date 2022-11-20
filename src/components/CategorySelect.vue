<script>
import { store } from '../data/store';
export default {
    name: 'CategorySelect',
    data() {
        return {
            store,
        };
    },
};
</script>

<template>
    <div class="container mb-4">
        <select
            @change="$emit('changeFilter')"
            v-model="store.filterWhitValue"
            class="form-select"
            aria-label="Default select example"
        >
            <option value="" selected>Select series</option>
            <option value="breaking bad">Breaking Bad</option>
            <option value="better call saul">Better Call Saul</option>
        </select>
    </div>
</template>

<style lang="scss" scoped>
.form-select {
    width: 160px;
}
</style>
