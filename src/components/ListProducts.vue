<script>
import SeriesCard from './SeriesCard.vue';

export default {
    name: "ListProducts",
    components: {
        SeriesCard,
    }
}
</script>

<template>
    <section>
        <div class="container">
            <h1> __Content goes here__ </h1>
            <SeriesCard />
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;

section {
    background-color: $tertiary;
    padding: 4rem;
}
</style>
