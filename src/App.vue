<template>
  <div id="app">
    <h3 class='h'>Click at screen were you will notice two components are communicating with each other using eventbus</h3>
    <test v-bind:header="header"/>
    <test2 v-bind:header="header"/>
    <hr />
    <h3 class='k'>using asyncawait and Setting a default value</h3>
    <asyncawaitdemo></asyncawaitdemo>
    <Settingadefaultvalue></Settingadefaultvalue>
  </div>
</template>

<script>
import asyncawaitdemo from './components/asyncawaitdemo.vue'
import Settingadefaultvalue from './components/Settingadefaultvalue.vue'
import test from './components/test.vue'
import test2 from './components/test2.vue'
export default {
  name: 'app',
  components: {
    test, test2, Settingadefaultvalue, asyncawaitdemo
  },
  data () {
    return {
      header: 'initial header'
    }
  }
}
</script>
<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.h{
color:blue;
text-decoration:underline;
}
.k{
color:orange;
text-decoration:underline;
}
</style>
