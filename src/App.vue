<template>
  <div>
    <bookOne></bookOne>
    <bookTwo></bookTwo>
    <button @click="minimizePrice" class="btn btn-success ml-5">Reduce Price</button>
  </div>
</template>

<script>
import bookOne from "@/components/bookOne";
import bookTwo from "@/components/bookTwo";
export default {
  name: 'App',
  components: {
    bookOne,
    bookTwo
  },
  methods:{
    minimizePrice(){
      // return this.$store.commit('reducePrice')
      return this.$store.dispatch('consizePrice')
    }
  }
}
</script>

<style>

</style>
