<script>
export default {
    name: "MenuNav",
}
</script>

<template>
    <section>
        <ul>
            <li>
                <a href="#">
                    <img src="../assets/images/buy-comics-digital-comics.png">
                    <p>DIGITAL COMICS</p>
                </a>
            </li>
            <li>
                <a href="#">
                    <img src="../assets/images/buy-comics-merchandise.png">
                    <p>DC MERCHANDISE</p>
                </a>
            </li>

            <li>
                <a href="#">
                    <img src="../assets/images/buy-comics-subscriptions.png">
                    <p>SUBSCRIPTION</p>
                </a>
            </li>
            <li>
                <a href="#">
                    <img src="../assets/images/buy-comics-shop-locator.png">
                    <p>COMIC SHOP LOCATOR</p>
                </a>
            </li>
            <li>
                <a href="#">
                    <img src="../assets/images/buy-dc-power-visa.svg">
                    <p>DC POWER VISA</p>
                </a>
            </li>
        </ul>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;

section {
    background-color: #0282f9;
    padding: 5rem;

    ul {
        list-style: none;
        @include center();

        li a {
            display: inline-block;
            text-decoration: none;
            padding: .5rem;
            color: #fff;

        }


    }
}
</style>
