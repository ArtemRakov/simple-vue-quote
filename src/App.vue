<template>
    <div class="container">
      <app-heading :quotes="quotes"> </app-heading>
      <app-create-quote :quotes="quotes"> </app-create-quote>
      <app-show-quote :quotes="quotes" @deleteQuote="deleteQuote"> </app-show-quote>
    </div>
</template>

<script>
  import Heading from "./components/Heading.vue"
  import CreateQuote from "./components/CreateQuote.vue"
  import ShowQuote from "./components/ShowQuote.vue"
    export default {
      data: function() {
        return {
          quotes: []
        }
      },
      methods: {
        deleteQuote(quote) {
          const index = this.quotes.indexOf(quote)
          this.quotes.splice(index, 1)
        }
      },
        components: {
          appHeading: Heading,
          appCreateQuote: CreateQuote,
          appShowQuote: ShowQuote
        }
    }
</script>

<style>
</style>
