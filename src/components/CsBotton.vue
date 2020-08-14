<template>
   <div>
   <h1> {{counter}}</h1>
  <div class="row">
    <div class="col-3">
     <button v-on:click="counter += 1"> <i class="far fa-thumbs-up"></i></button>
   </div>
     <div class="col-3">
     <button v-on:click="counter -= 10"><i class="far fa-thumbs-down"></i></button>
   </div>
     <div class="col-3">
     <button v-on:click="counter += 10"><i class="far fa-heart"></i></button>
   </div>
     <div class="col-3">
     <button v-on:click="counter = 0"><i class="fas fa-retweet"></i></button>
  </div>
  </div>
  </div>
</template>

<script>
export default {
    name: 'CsBotton',
    props: {
        lebel: String,
    },
    data: function() {
  return{
    counter: 0,
    }
  }
}
</script>

<style>

</style>