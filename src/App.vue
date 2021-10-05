<template>
  <div>
    <!-- <Hello /> -->
    <!-- <Question3 /> -->
    <!-- <Clock /> -->
    <Weather />

    
  </div>

</template>

<script>
// import Calculator from './components/Calculator.vue';
//  import Clock from './components/Clock.vue';
import Weather from './components/Weather.vue';
// import Hello from "./components/Hello.vue"
 //import QuestionTwo from "./components/QuestionTwo.vue"
  // import Question3 from "./components/Question3.vue"

export default {
  name: 'App',
  components:{

    Weather,

  },  
};
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
</style>
