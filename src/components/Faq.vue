<template>
    <div class="faq">
        <div class="container">
            <section class="section">
                <h1 class="title">FAQ</h1>
                <h2
                    class="subtitle is-4"
                >Commodo laboris excepteur enim et proident eu deserunt non occaecat.</h2>

                <div class="columns" v-if="faqs && faqs.length">
                    <div class="column is-one-third" v-for="faq of faqs" :key="faq.id">
                        <div class="card">
                            <div class="card-content">
                                <p class="title">{{ faq.title }}</p>
                                <p class="answer">{{ faq.body }}</p>
                            </div>
                        </div>
                    </div>
                </div>
            </section>
        </div>
    </div>
</template>

<script>
import axios from 'axios'

export default {
    name: 'faq',
    data: () => ({
        faqs: [],
        errors: [],
    }),
    created() {
        axios
            .get('https://jsonplaceholder.typicode.com/posts')
            .then(result => {
                this.faqs = result.data.slice(0, 10)
            })
            .catch(e => {
                this.errors.push(e)
            })
    },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="sass">
@import '../main.sass'

.pd
    padding: 2.5rem 0 1.5rem 0

.answer
    margin-top: 10px !important
    color: gray

.columns
    flex-wrap: wrap
</style>
