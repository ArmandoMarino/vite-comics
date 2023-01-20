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
                <h3>DC COMICS</h3>
                <ul>
                    <li v-for="link in links">{{ link.text }}</li>
                </ul>
                <h3>SHOP</h3>
                <ul>
                    <li v-for="shoplink in shoplinks">{{ shoplink.text }}</li>
                </ul>
            </nav>

        </section>
    </footer>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/mixins' as *;

ul {

    li {
        list-style-type: none;
        font-size: 12px;

        a {
            text-transform: uppercase;
        }
    }
}
</style>