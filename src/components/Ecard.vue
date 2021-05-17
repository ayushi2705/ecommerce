<template>
  <div class="event-card">
    <div class="card">
    </div>
      <div class="card-content">
        <h2 class="is-size-4 ">{{ product.displayName }}</h2>
        <p class="is-size-5 "> Price:  &#8377; {{ product.price }}</p>
        <p class="is-size-5"> Ratings:  {{ product.avgRating }}/5  </p>
      </div>
    </div>
</template>


<script>
export default {
  props: [
    'product'
  ]
}
</script>


<style lang="scss" scoped>
  .card {
    background-image: url('https://minutebag.com/wp-content/uploads/2018/10/ariel-matic-fl-2kg1.gif');
    height: 300px;
    background-position: center;
    background-size: cover;
    text-align: center;
  }
  .card-content {
    padding-top: 50px;
    background-color:white;
    padding: 5px;
    height: 160px;
    color:black;
    font-family: Georgia, Times New Roman, Times, serif;;
    text-decoration: underline white !important;
  }
  .event-card{
     box-shadow: 3px 2px 5px 0px #969696;
  }

</style>