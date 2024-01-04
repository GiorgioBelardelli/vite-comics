<script>
export default {
    name: "AppHeader",
    data() {
        return {
            links: [
                {
                    text: "CHARACTERS",
                    url: "#",
                    current: false,
                },
                {
                    text: "COMICS",
                    url: "#",
                    current: true,
                },
                {
                    text: "MOVIES",
                    url: "#",
                    current: false,
                },
                {
                    text: "TV",
                    url: "#",
                    current: false,
                },
                {
                    text: "GAMES",
                    url: "#",
                    current: false,
                },
                {
                    text: "COLLECTIBLES",
                    url: "#",
                    current: false,
                },
                {
                    text: "VIDEOS",
                    url: "#",
                    current: false,
                },
                {
                    text: "FANS",
                    url: "#",
                    current: false,
                },
                {
                    text: "NEWS",
                    url: "#",
                    current: false,
                },
                {
                    text: "SHOP",
                    url: "#",
                    current: false,
                },
            ]
        }
    }
}
</script>

<template>
    <header>

        <!-- logo -->
        <a href="#">
            <img src="/dc-logo.png" alt="DC Logo">
        </a>

        <!-- menu di navigazione -->

        <nav>
            <ul>
                <li v-for="link in  links">
                    <a :href="link.url" :class="link.current ? 'active' : ''">
                        {{ link.text }}
                    </a>
                </li>

            </ul>
        </nav>

    </header>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;

header {
    background-color: $primary;
    margin-top: 3rem;

    ul {
        list-style: none;
        @include center();

        li a {
            display: inline-block;
            text-decoration: none;
            padding: 0;
            margin: 1rem;

            &.active,
            &:hover {
                border-bottom: 7px solid $secondary;
                color: $secondary;
            }
        }


    }
}
</style>
