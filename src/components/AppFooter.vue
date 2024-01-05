<script>
export default {
    name: "AppFooter",
    data() {
        return {
            icons: [
                {
                    src: "/footer-facebook.png",
                    alt: "facebooklogo"
                },
                {
                    src: "/footer-periscope.png",
                    alt: "periscopelogo"
                },
                {
                    src: "/footer-pinterest.png",
                    alt: "pinterestlogo"
                },
                {
                    src: "/footer-twitter.png",
                    alt: "twitterlogo"
                },
                {
                    src: "/footer-youtube.png",
                    alt: "youtubelogo"
                }
            ]
        }

    }

}
</script>

<template>
    <section id="top-footer">
        <div class="container">
            <div class="row">
                <div class="col">
                    <ul>
                        <h3>DC COMICS</h3>
                        <li><a href="#">Characters</a></li>
                        <li><a href="#">Comics</a> </li>
                        <li><a href="#">Movies</a> </li>
                        <li><a href="#">TV</a> </li>
                        <li><a href="#">Games</a> </li>
                        <li><a href="#">Videos</a> </li>
                        <li><a href="#">News</a> </li>
                        <h3>SHOP</h3>
                        <li><a href="#">Shop DC</a></li>
                        <li><a href="#">Shop DC Collectibles</a> </li>
                    </ul>
                    <ul>
                        <h3>DC</h3>
                        <li><a href="#">Terms Of Use</a></li>
                        <li><a href="#">Privacy policy(New)</a></li>
                        <li><a href="#">Ad Choices</a></li>
                        <li><a href="#">Advertising</a></li>
                        <li><a href="#">Jobs</a></li>
                        <li><a href="#">Subscriptions</a></li>
                        <li><a href="#">Talent Workshops</a></li>
                        <li><a href="#">CPSC Certificate</a></li>
                        <li><a href="#">Ratings</a></li>
                        <li><a href="#">Shop Help</a></li>
                        <li><a href="#">Contact Us</a></li>
                    </ul>
                    <ul>
                        <h3>SITES</h3>
                        <li><a href="#">DC</a></li>
                        <li><a href="#">MAD Magazine</a></li>
                        <li><a href="#">DC Kids</a></li>
                        <li><a href="#">DC Universe</a></li>
                        <li><a href="#">DC Power Visa</a></li>
                    </ul>
                </div>
                <div class="col">
                    <img src="../assets/images/dc-logo-bg.png" alt="DCicon">
                </div>
            </div>
        </div>
    </section>
    <div id="bot-footer">
        <div class="container">
            <div class="row">
                <div class="col">
                    <a href="#">
                        SIGN-UP NOW!
                    </a>
                </div>
                <div class="col">
                    <ul>
                        <li>
                            <a href="#">
                                FOLLOW US
                            </a>
                        </li>

                        <li v-for="icon in  icons ">
                            <a href="#">
                                <img :src="icon.src" :alt="icon.alt">
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;

section {
    background-image: url(../assets/images/footer-bg.jpg);
    background-size: cover;

    .col img {}


    ul {
        display: inline-block;
        vertical-align: top;
        margin: 3rem 1rem;

        h3 {
            margin: 1.5rem 0;
        }

        li {
            margin: .5rem 0;

            a {
                color: #959595;
            }
        }
    }
}


a {
    text-decoration: none;
}

ul {
    list-style: none;
}

.row {
    @include center(horizontal);
    justify-content: space-between;
}

#bot-footer {

    background-color: $quaternary;
    padding: 4rem;
    font-size: 20px;

    a {
        color: $primary;
        margin: 0 .5rem;
        border: 3px solid $secondary;
        padding: 1rem;
    }


    ul {
        @include center();

        li a {
            color: $secondary;
            border: 0;
            padding: 0;
        }
    }
}
</style>