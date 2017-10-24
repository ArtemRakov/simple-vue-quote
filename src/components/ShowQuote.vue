<template>
  <div class="wrapper">  
    <div class="row">     
      <div class="col-xs-2"  v-for="quote in quotes" @click="deleteQuote(quote)">
        <div class="card" style="cursor: pointer;">
          <p> {{quote}} </p>
        </div>
      </div>
    </div>    
  </div>
</template>

<script>
    export default {
      props: ['quotes'],
      methods: {
        deleteQuote(quote) {
          const index = this.quotes.indexOf(quote)
          this.quotes.splice(index, 1)
        }
      }
    }
</script>

<style scoped>
  .wrapper {
    margin-top: 30px;
  }
  .cards {
    display: flex;
  }
  .card {
    height: 100px;
    background-color: #F6F6F6;
    font-style: italic;
    display: flex;
    align-items: center;
    justify-content: space-around;
    margin: 5px 0px;
    border-radius: 10px;
  }
  p {
    font-size: 20px;
    font-family: "Arizonia";
    font-weight: bold;
    margin: 0 5px;
  }
</style>
