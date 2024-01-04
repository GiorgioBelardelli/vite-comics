<script>
export default {
    name: "AppFooter",
}
</script>

<template>
    <section id="top-footer">
        <h1> __Content goes here__ </h1>
    </section>
    <div id="bot-footer">

    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;

section {
    background-image: url(../assets/images/footer-bg.jpg);
}

#bot-footer {
    background-color: $quaternary;
    padding: 4rem;
}
</style>