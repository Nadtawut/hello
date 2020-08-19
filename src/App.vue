<template>

  <div class="row-12">
  <div id="app">
    <div class="col">
    <img alt="me" src="./images/me1.jpg" width ="20%">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  
      <div class="col"> <Counter lable="ok" @cc="sum"/> </div>
     <CsBotton/>
    </div>  
    <div class="col">
      <img alt="me" src="./images/mypro.jpg" width ="20%">
      <HelloWorld msg="Welcome to Your Vue.js App"/>
        <div class="col"> <Counter lable="ok" @cc="sum"/> </div>
       <CsBotton/>
      </div>  
      <div class="col">
        <img alt="me" src="./images/myproa3.jpg" width ="20%">
        <HelloWorld msg="Welcome to Your Vue.js App"/>
          <div class="col"> <Counter lable="ok" @cc="sum"/> </div>
         <CsBotton/>
        </div>  
   
    <div>
      ชื่อ-นามสกุล <input type="text" v-model="name"/>
      รหัส นศ. <input type="text " v-model="code">
      GPA <input type="number" v-model="gpa" step="0.01"/>
      <hr>
      แสดง ชื่อ + รหัส นศ. gpa 
    {{name}} {{code}} {{gpa}}
  </div>
</div>
</div>


</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import CsBotton from './components/Csbotton'
export default {
  name: 'App',
  components: {
    HelloWorld,
    CsBotton,
  },
  data :function(){
    return{
    total:0,
    name:'',
    code:'',
    gpa:'',
    };
  },

  methods: {
    
    sum(counterValue) {
      this.total += counterValue
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
  text:center;
}
</style>