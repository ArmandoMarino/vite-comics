<script>
export default {
    name: 'AppJumbo',
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
        <!-- BLACKBOARD -->
        <section id="contents-space">
            <div class="blackboard">
                <h3>--> Content goes here </h3>
            </div>
        </section>

        <!-- CENTER NAV -->
        <section id="center-nav">
            <nav class="container">
                <!-- LINK LIST -->
                <ul>
                    <!-- TODO v-for -->
                    <li></li>
                </ul>
            </nav>
        </section>
    </main>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/mixins' as *;

#contents-space {
    .blackboard {
        @include flex-between;
        min-height: 100px;
        background-color: black;

        h3 {
            color: white;
            margin-left: 15rem;
        }
    }
}


#center-nav {
    min-height: 140px;
    background-color: #0282f9;
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