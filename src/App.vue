<template>
    <div id="app">
        <nav class="navbar" role="navigation" aria-label="main navigation">
            <div class="navbar-brand">
                <a class="navbar-item" href="https://bulma.io">
                    <img src="https://bulma.io/images/bulma-logo.png" width="112" height="28" />
                </a>

                <a
                    role="button"
                    class="navbar-burger burger"
                    aria-label="menu"
                    aria-expanded="false"
                    data-target="navbarBasicExample"
                    v-on:click="toggleNav()"
                    v-bind:class="{ 'is-active': isActive }"
                >
                    <span aria-hidden="true"></span>
                    <span aria-hidden="true"></span>
                    <span aria-hidden="true"></span>
                </a>
            </div>

            <div
                id="navbarBasicExample"
                class="navbar-menu"
                v-bind:class="{ 'is-active': isActive }"
            >
                <div class="navbar-end">
                    <router-link to="/" class="navbar-item">Home</router-link>
                    <router-link to="faq" class="navbar-item">FAQ</router-link>

                    <div class="navbar-item">
                        <div class="buttons">
                            <a class="button is-primary is-outlined">
                                <i class="fa fa-download"></i>
                                <span>Join now</span>
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </nav>
        <router-view />

        <footer class="footer is-primary">
            <div class="container">
                <div class="columns">
                    <div class="column">This is some text</div>
                    <div class="column has-text-right">
                        <a href="#" class="icon">
                            <i class="fa fa-edit"></i>
                        </a>
                        <a href="#" class="icon">
                            <i class="fa fa-times"></i>
                        </a>
                    </div>
                </div>
            </div>
        </footer>
    </div>
</template>

<script>
export default {
    name: 'App',
    data: function() {
        return { isActive: false }
    },
    methods: {
        toggleNav: function() {
            this.isActive = !this.isActive
        },
    },
}
</script>

<style lang="sass">
@import '../node_modules/bulma/bulma.sass'
@import 'main'

.navbar
    background-color: #383838
    a:hover
        color: gray

.navbar-end a
    color: #C1C1C1
    padding: 0.5rem 1.75rem
    +mobile
        color: gray
        &::hover
            background-color: #F1F1F1

.navbar-burger span
    background-color: #C1C1C1

footer
    background-color: $primary !important
    color: #fff

.icon
    color: #fff
    margin-left: 20px
</style>
