<script>
export default {
    name: 'AppHeader',
    props: {
        title: String,
    },
};
</script>

<template>
    <header class="p-2 mb-5">
        <h1>{{ title }}</h1>
    </header>
</template>

<style lang="scss" scoped>
h1 {
    font-weight: 600;
}
</style>
