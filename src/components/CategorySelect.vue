<script>
export default {
    name: 'CategorySelect',
};
</script>

<template>
    <div class="container mb-4">
        <select class="form-select" aria-label="Default select example">
            <option selected>Select category</option>
            <option value="1">One</option>
            <option value="2">Two</option>
            <option value="3">Three</option>
        </select>
    </div>
</template>

<style lang="scss" scoped>
.form-select {
    width: 160px;
}
</style>
