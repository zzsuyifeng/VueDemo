<template>
  <div id="app">
    <h1>父组件子组件相互传值</h1>
    <h5>简单 / 易用 / 便捷</h5>
    <!-- 子组件向父组件传值 -->
    <translate-from v-on:translateForm="translateFormAction"></translate-from>
    <!-- 父组件向子组件传值 -->
    <translate-out :textOut="textTranslate"></translate-out>
  </div>
</template>

<script>
import TranslateFrom from './components/TranslateFrom'
import TranslateOut from './components/TranslateOut'

export default {
  name: 'App',
  data(){
    return{
      textTranslate:''
    }
  },
  components:{
    'translate-from':TranslateFrom,
    'translate-out':TranslateOut
  },
  methods:{
    // 子组件传过来的值
    translateFormAction(text){
      this.textTranslate = text;
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
</style>
