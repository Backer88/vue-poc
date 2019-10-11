<template>
    <div class="hero">
        <section class="hero is-medium is-danger is-bold">
            <div class="hero-body">
                <div class="container">
                    <h1 class="title">{{ heading }}</h1>
                    <div class="is-two-thirds column is-paddingless">
                        <h2 class="subtitle is-4">{{ subheading }}</h2>
                    </div>
                    <a class="button is-large" id="learn">Learn more</a>
                </div>
            </div>
        </section>

        <section class="section">
            <div class="container">
                <div class="columns pd is-desktop">
                    <div class="column is-1 has-text-centered">
                        <i class="fa fa-cog is-primary"></i>
                    </div>
                    <div class="column is-one-third-desktop">
                        <p class="title">
                            <strong>Ullamco est eiusmod sunt Lorem velit enim in commodo adipisicing velit in laborum nulla.</strong>
                        </p>
                    </div>
                    <div class="column">
                        <p>Deserunt commodo minim eiusmod Lorem minim excepteur dolore.</p>
                    </div>
                </div>
            </div>

            <div class="columns pd">
                <div class="column">
                    <div class="card">
                        <div class="card-content">
                            <p
                                class="title"
                            >“There are two hard things in computer science: cache invalidation, naming things, and off-by-one errors.”</p>
                            <p class="subtitle">- Jeff Atwood</p>
                        </div>
                    </div>
                </div>
                <div class="column">
                    <div class="card">
                        <div class="card-content">
                            <p
                                class="title"
                            >“There are two hard things in computer science: cache invalidation, naming things, and off-by-one errors.”</p>
                            <p class="subtitle">- Jeff Atwood</p>
                        </div>
                    </div>
                </div>
                <div class="column">
                    <div class="card">
                        <div class="card-content">
                            <p
                                class="title"
                            >“There are two hard things in computer science: cache invalidation, naming things, and off-by-one errors.”</p>
                            <p class="subtitle">- Jeff Atwood</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </div>
</template>

<script>
export default {
    name: 'home',
    data: function() {
        return {
            heading: 'Home',
            subheading: 'Subheading',
        }
    },
    methods: {
        learnMore: function() {},
    },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="sass">
@import '../main.sass'

h2
    margin: 1.5rem 0 2rem 0 !important

.fa-cog
    font-size: 40px

#learn
    +desktop
    margin-bottom: 2rem

.pd
    +tablet
        padding: 2rem 0
</style>
