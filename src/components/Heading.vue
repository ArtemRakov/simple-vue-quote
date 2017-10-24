<template>
    <div class="top">
      <h2> Quotes Added </h2>
      <div class="bar">
        <div v-if="quotes.length > 0" class="progress" :style="{width: (quotes.length * 10) + '%'}">
          <p> {{quotes.length}} / 10 </p>
        </div>
        <div v-else class="no-quotes">
          <p> No quotes</p>
        </div>
      </div>
    </div>
</template>

<script>
    export default {
      props: ['quotes']
    }
</script>

<style scoped>
  .top {
    margin-top: 50px;
  }
  .bar {
    width: 100%;
    background-color: #F6F6F6;
  }
  .progress {
    background-color: #4D8ABB;
  }
  p {
    text-align: center;
  }

  .no-quotes {
    width: 100%;
    background-color: #F6F6F6;
  }
</style>
