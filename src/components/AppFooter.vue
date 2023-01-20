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

            </nav>

        </section>
    </footer>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/mixins' as *;

#footer-links {
    max-height: 300px;

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
        }
    }
}
</style>