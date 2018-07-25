<template>
    <div id="translateOut">
        <!-- 子组件获取父组件传过来的值 -->
        {{this.textOut}}
    </div>
</template>

<script>
export default {
    name:'translateOut',
    props:['textOut'],
    data(){
        return{

        }
    }
}
</script>

<style scoped>

</style>
