<script>
export default {
    name: 'AppFooter',
    data() {
        return {
            links: [

                {
                    text: 'Characters',
                    url: '#',
                },
                {
                    text: 'Comics',
                    url: '#',
                },
                {
                    text: 'Movies',
                    url: '#',
                },
                {
                    text: 'TV',
                    url: '#',
                },
                {
                    text: 'Games',
                    url: '#',
                },
                {
                    text: 'Collectibles',
                    url: '#',
                },
                {
                    text: 'Videos',
                    url: '#',
                },
                {
                    text: 'Fans',
                    url: '#',
                },
                {
                    text: 'News',
                    url: '#',
                },
                {
                    text: 'Shop',
                    url: '#',
                },
            ],
            shoplinks: [
                {
                    text: 'shop dc',
                    url: '#',

                },
                {
                    text: 'Comics',
                    url: '#',
                },
            ],
            dclinks: [
                {
                    text: 'terms of use',
                    url: '#',
                },
                {
                    text: 'privacy policy',
                    url: '#',
                },
                {
                    text: 'ad chaices',
                    url: '#',
                },
                {
                    text: 'advertising',
                    url: '#',
                },
                {
                    text: 'jobs',
                    url: '#',
                },
                {
                    text: 'subscriptions',
                    url: '#',
                },
                {
                    text: 'talent workshop',
                    url: '#',
                },
                {
                    text: 'certificates',
                    url: '#',
                },
                {
                    text: 'ratings',
                    url: '#',
                },
                {
                    text: 'Shop help',
                    url: '#',
                },
                {
                    text: 'contact us',
                    url: '#',
                }
            ],
            siteslinks: [
                {
                    text: 'DC',
                    url: '#',
                },
                {
                    text: 'mad magazine',
                    url: '#',
                },
                {
                    text: 'DC kids',
                    url: '#',
                },
                {
                    text: 'DC universe',
                    url: '#',
                },
                {
                    text: 'DC power visa',
                    url: '#',
                },
            ],
        }
    }
}
</script>

<template>
    <footer>
        <!-- NAV LINKS -->
        <section id="footer-links" class="container">
            <nav>
                <div class="links-left">

                </div>
                <!-- COL LEFT -->
                <div class="col">
                    <h3>DC COMICS</h3>
                    <ul>
                        <li v-for="link in links">
                            <a :href="link.url">{{ link.text }}</a>
                        </li>
                    </ul>
                    <h3>SHOP</h3>
                    <ul>
                        <li v-for="shoplink in shoplinks">
                            <a :href="shoplink.url">{{ shoplink.text }}</a>
                        </li>
                    </ul>
                </div>

                <!-- COL CENTER -->
                <div class="col">
                    <h3>DC</h3>
                    <ul>
                        <li v-for="dclink in dclinks">
                            <a :href="dclink.url">{{ dclink.text }}</a>
                        </li>
                    </ul>
                </div>

                <!-- COL RIGHT -->
                <div class="col">
                    <h3>SITES</h3>
                    <ul>
                        <li v-for="siteslink in siteslinks">
                            <a :href="siteslink.url">{{ siteslink.text }}</a>
                        </li>
                    </ul>
                </div>

                <div id="big-logo">

                </div>
            </nav>

        </section>

        <!-- SOCIALS -->
        <section id="footer-socials">
            <div id="wrapper" class="container">
                <div id="sign-up">
                    <h3>SIGN-UP NOW!</h3>
                </div>

                <div id="follow">
                    <h3>FOLLOW US</h3>
                    <a href="#"><i class="fa-brands fa-2xl fa-facebook"></i></a>
                    <a href="#"><i class="fa-brands fa-2xl fa-twitter"></i></a>
                    <a href="#"><i class="fa-brands fa-2xl fa-youtube"></i></a>
                    <a href="#"><i class="fa-brands fa-2xl fa-pinterest"></i></a>
                    <a href="#"><i class="fa-solid fa-2xl fa-location-dot"></i></a>
                </div>
            </div>

        </section>
    </footer>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/mixins' as *;
@use '../assets/scss/partials/variables' as *;

// NAV LINKS FOOTER-UP
footer {
    background-image: url(../assets/img/footer-bg.jpg);
}

#footer-links {
    max-height: 300px;
    color: white;

    nav {
        display: flex;
    }

    .col {
        flex-basis: 15%;
        margin-top: 10px;
    }
}

ul {
    margin-bottom: 10px;

    li {
        list-style-type: none;
        font-size: 12px;

        a {
            text-transform: capitalize;
            color: grey;
        }
    }
}

#big-logo {
    width: 100%;
    background-image: url(../assets/img/dc-logo-bg.png);
    background-position: center;
    background-repeat: no-repeat;
    background-size: 60%;
}


// SOCIALS FOOTER-BOTTOM
#footer-socials {
    background-color: $grey;
    height: 100px;

    #wrapper {
        @include flex-between;
        height: 100%;
    }

    #sign-up {
        padding: 10px;
        border: 2px $primaryblue solid;
        text-align: center;

        h3 {
            font-size: 15px;
            color: grey;
        }
    }

    #follow {
        @include flex-between;

        h3 {
            font-size: 15px;
            padding: 10px;
            color: $primaryblue;
        }

        a {
            color: gray;
            padding: 5px;
        }
    }
}
</style>