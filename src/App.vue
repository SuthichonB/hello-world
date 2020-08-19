<template>
  <div id="app">
    <h1>{{t1+t2+t3}}</h1>
    <div class="row">
      <div class="col-4"> 
      <img src="https://i.pinimg.com/originals/78/ac/aa/78acaad3c2890c0d47f94ec7b3cce9fb.jpg" height="350" alt="">
      <CsBotton @cc="sum1"/>
      </div>  
      <div class="col-4"> 
      <img src="https://vignette.wikia.nocookie.net/marvelcinematicuniverse/images/6/63/97d1d9f934a350cee765c5ac1a466605.jpg/revision/latest?cb=20190527184444" height="350" alt="">
      <CsBotton @cc="sum2"/>
      </div> 
      <div class="col-4 " > 
      <img src="https://www.kindpng.com/picc/m/98-989089_jotaro-kujo-part-3-hd-png-download.png" height="350" alt="">
      <CsBotton @cc="sum3"/>
      </div>   
  </div><br>
  <!----ชื่อ สกึล รหัส GPA--->
    ชื่อ-นามสกุล
    <input type="text" v-model="name" />
    รหัสนักศึกษา
    <input type="text" v-model="code" />
    GPA
    <input type="number" v-model="gpa" step="0.01" />
    <hr />

    แสดงชื่อ + นามสกุล + รหัสนักศึกษา + GPA
    {{name}} {{code}} {{gpa}}
  </div>
</template>

<script>
import CsBotton from './components/CsBotton.vue'

export default {
  name: 'App',
  components: {
    CsBotton,
    
  },
  data: function() {
      return{
        total : 0,
        t1 : 0,
        t2 : 0,
        t3 : 0,
        name: "",
        code: "",
        gpa: 0.1, 
      }
    },
  methods: {
    sum1(counterValue){
      this.t1 = counterValue
    },
    sum2(counterValue){
      this.t2 = counterValue
    },
    sum3(counterValue){
      this.t3 = counterValue
    },
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.col-4{
  border: 1px solid red;
}
</style>
