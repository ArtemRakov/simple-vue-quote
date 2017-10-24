<template>
  <div class="wrapper">  
    <div class="row">
      <div class="col-xs-6 col-xs-offset-3">
        <div class="form-group quote-form">
          <label for="quote">Quote </label>
          <textarea class="form-control" rows="4" cols="50" v-model="context"></textarea>
          <button class="btn btn-primary" @click="createQuote"> Add quote </button>
        </div>
      </div>     
    </div>
  </div>
</template>

<script>
    export default {
      props: ["quotes"],
      data: function() {
        return {
          context: ""
        }
      },
      methods: {
        createQuote() {
          if (this.quotes.length < 10) {
            this.quotes.push(this.context)
            this.context = ""
          }
          else {
            alert("Too many quotes")
          }
        }
      }
    }
</script>

<style scoped>
  .wrapper {
    margin-top: 30px;
  }
  button {
    text-align: center;
    display: block;
    margin: 10px auto;
  }
</style>
