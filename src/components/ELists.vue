<template>
  <div class="events container">
    <h2 class="subtitle is-3">
    Check out our upcoming events
    </h2>
    <div class="columns is-multiline">
      <div class="column is-one-quarter">
          <Ecard />
      </div>
    </div>
  </div>
</template>
<script>
  import Ecard from '@/components/Ecard';
  export default {
    name: 'ELists',
    components : {
      Ecard
    }
  }
</script>
<style lang="scss" scoped>
  .events {
    margin-top: 100px;
    text-align: center;
  }
</style>