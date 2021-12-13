<template>
  <div class="container">
    <div class="row bg-info text-white mt-4 px-4 py-4">
      <div class="col-12">
        <div v-for="book in cutPrice" :key="book.id">
          <span>{{ book.name }}</span>
          <span class="text-white"> ${{ book.price }}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

import {mapGetters} from "vuex";

export default {
  computed: {
    books(){
      return this.$store.state.books
    },
    // cutPrice(){
    //   return this.$store.getters.cutPrice
    // }

    ...mapGetters([
      'cutPrice'
    ])
  }
}
</script>

<style scoped>

</style>