<template>
  <div>
    <h1>{{counter}}</h1>
  <div class="row">
    <div class="col-3">
     <button v-on:click="upFunction"> <i class="far fa-thumbs-up"></i></button>
   </div>
     <div class="col-3">
     <button v-on:click="downFunction"><i class="far fa-thumbs-down"></i></button>
   </div>
     <div class="col-3">
     <button v-on:click="LFunction"><i class="far fa-heart"></i></button>
   </div>
     <div class="col-3">
     <button v-on:click="reFunction"><i class="fas fa-retweet"></i></button>
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
        fsize: 50,
        
      }
    },

    methods: {
   upFunction : function(){
      this.counter += 1
      this.fsize += 10
      this.$emit('cc', this.counter)
   },
   downFunction : function(){
      this.counter -= 1
      this.fsize -= 10
      this.$emit('cc', this.counter)
   },
   LFunction : function(){
      this.counter += 10
      this.fsize += 10
      this.$emit('cc', this.counter)
   },
   reFunction : function(){
      this.counter = 0
      this.fsize = 50
      this.$emit('cc', this.counter)
   },
  
  }
}
</script>

<style>

</style>