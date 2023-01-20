<script>
export default {
    name: 'AppHeader',
    data() {
        return {
            links: [

                {
                    text: 'Characters',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Comics',
                    url: '#',
                    current: true,
                },
                {
                    text: 'Movies',
                    url: '#',
                    current: false,
                },
                {
                    text: 'TV',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Games',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Collectibles',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Videos',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Fans',
                    url: '#',
                    current: false,
                },
                {
                    text: 'News',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Shop',
                    url: '#',
                    current: false,
                },


            ]
        }
    }
}
</script>

<template>
    <header class="container">
        <figure id="logo-header">
            <a href="#">
                <img src="../assets/img/dc-logo.png" alt="DC_Logo">
            </a>
        </figure>
        <nav>
            <ul>
                <li v-for="link in links" :key="link.text">
                    <a :href="link.url">{{ link.text }}</a>
                </li>
            </ul>
        </nav>
    </header>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/mixins' as *;

#logo-header {
    padding: 1rem;

    img {
        width: 70px;
        height: 70px;
    }
}

header {
    @include flex-between;

}

nav {
    flex-direction: row;
    flex-basis: calc(100%/4);
    width: 100%;
}

ul {
    @include flex-between;

    li {
        list-style-type: none;
        font-size: 10px;
        padding: 10px;

        a {
            text-transform: uppercase;
        }
    }
}
</style>