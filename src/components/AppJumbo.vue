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
    }
}
</script>

<template>
    <main>
        <section id="contents-space">
            <div class="blackboard">
                <h3>--> Content goes here </h3>
            </div>
        </section>

        <section>
            <nav>
                <ul>
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
</style>