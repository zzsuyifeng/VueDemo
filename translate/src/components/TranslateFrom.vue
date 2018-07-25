<template>
    
<div id="translateFrom">
    <input type="text" placeholder="请输入内容" v-model="translateText"><br>
    <button v-on:click="fromSubmit">提交</button>
</div>

</template>

<script>
// 获取版本号
import pakage from '../../package.json'

export default {
  name: "translateFrom",
  data() {
    return {
      translateText: ""
    };
  },
  methods: {
    fromSubmit() {
      // 向父组件传值
      this.$emit("translateForm", this.translateText);
      // 获取版本号
      console.log(pakage.version);
    }
  }
};
</script>

<style scoped>
input{
  margin: 5px 0;
  width: 200px;
  height: 30px;
  border: 1px solid #555;
}
button{
  margin: 10px 0;
  width: 50px;
  height: 50px;
  background-color: aqua;
  border: 1px solid #333;
}
</style>
