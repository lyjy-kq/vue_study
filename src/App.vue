<template>
        <Person/>
</template>

<script lang="ts">
    import Person from './components/Person.vue'

    export default{
        name:'app', //组件名
        components:{Person} //注册组件
    }
</script>

<style>
    .app {
        background-color: #dddddd;
        box-shadow: 0 0 10px;
        border-radius: 10px;
        padding: 20px;
    }
</style>