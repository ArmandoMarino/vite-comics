<script>
import ProductsCard from './products/ProductsCard.vue';
export default {
    name: 'AppJumbo',
    components: {
        ProductsCard
    },
    props: {
        products: Array
    },
    data() {
        return {
            links: [

                {
                    text: 'digital comics',
                    url: '#',
                    current: false,
                },
                {
                    text: 'dc merchandise',
                    url: '#',
                    current: true,
                },
                {
                    text: 'subscription',
                    url: '#',
                    current: false,
                },
                {
                    text: 'comic shop locator',
                    url: '#',
                    current: false,
                },
                {
                    text: 'dc power visa',
                    url: '#',
                    current: false,
                },
            ],
            jumboimages: [
                {
                    text: 'digital comics',
                    image: 'buy-comics-digital-comics.png',
                    url: '#',
                    current: false,
                },
                {
                    text: 'dc merchandise',
                    image: 'buy-comics-merchandise.png',
                    url: '#',
                    current: false,
                },
                {
                    text: 'subscription',
                    image: 'buy-comics-subscriptions.png',
                    url: '#',
                    current: false,
                },
                {
                    text: 'comic shop locator',
                    image: 'buy-comics-shop-locator.png',
                    url: '#',
                    current: false,
                },
                {
                    text: 'dc power visa',
                    image: 'buy-dc-power-visa.svg',
                    url: '#',
                    current: false,
                },

            ]
        }
    },
    methods: {
        buildImagePath(image) {
            const url = new URL(`../assets/img/${image}`, import.meta.url);
            return url.href;
        }
    }
}
</script>

<template>
    <main>
        <div class="image-main">
            <img src="../assets/img/jumbotron.jpg" alt="Teen Titans">
        </div>

        <!-- BLACKBOARD PRODUCTS LIST -->
        <section id="contents-space">
            <div class="blackboard">
                <ProductsCard v-for="product in products" :key="product.thumb" :product="product" />
            </div>
        </section>

        <!-- CENTER NAV -->
        <section id="center-nav">
            <nav class="container">
                <!-- LINK LIST -->
                <ul>
                    <li v-for="jumboimage in jumboimages">
                        <a :href="jumboimage.url">
                            <img :src="buildImagePath(jumboimage.image)" alt="">
                            {{ jumboimage.text }}
                        </a>
                    </li>
                </ul>
            </nav>
        </section>
    </main>
</template>

<style lang="scss" >
@use '../assets/scss/partials/mixins' as *;
@use '../assets/scss/partials/variables' as *;

// IMAGE-MAIN
.image-main {
    img {
        width: 100%;
        height: 300px;
        object-fit: cover;
        object-position: top;
    }
}


// PRODUCTS
#contents-space {
    background-color: black;

    .blackboard {
        margin: 0 auto;
        max-width: 1000px;
        display: flex;
        flex-wrap: wrap;
        min-height: 100px;

        .product-card {
            flex-basis: calc(100% / 6);

            p {
                color: white;
                display: block;
            }
        }



        h3 {
            color: white;
            margin-left: 15rem;
        }
    }
}

// CENTER NAV
#center-nav {
    @include flex-between;
    min-height: 140px;
    background-color: $primaryblue;

    ul {
        @include flex-between;

        li {

            list-style-type: none;
            font-size: 10px;
            padding: 30px;

            a {
                @include flex-between;
                color: white;
                text-transform: uppercase;

                img {
                    margin: 7px;
                    width: 40px;
                }
            }
        }
    }
}
</style>