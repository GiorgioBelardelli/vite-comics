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
        <div class="container">
            <section>
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
            </section>

        </div>
    </header>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;

header {
    background-color: $primary;
    font-weight: 500;

    section {
        @include center(horizontal);
        justify-content: space-between;
        padding: 1rem 0;

    }

    ul {

        list-style: none;
        @include center();
        border: 1px dashed black;

        li {
            border: 1px dashed black;
        }

        li a {
            font-size: 14px;
            text-decoration: none;
            margin: 0 1rem;
            padding: auto 0;
            color: #46464c;
            border: 1px dashed black;

            &.active,
            &:hover {
                border-bottom: 7px solid $secondary;
                color: $secondary;
            }
        }


    }
}
</style>
