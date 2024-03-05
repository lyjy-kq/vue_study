<template>
    <div class="person">
        <h2>姓名：{{ name }}</h2>
        <h2>年龄：{{ age }}</h2>
        <button @click="changeName">修改名字</button>
        <button @click="changeAge">修改年龄</button>
        <button @click="showTel">查看联系方式</button>
    </div>
</template>

<script lang="ts">
    export default{
        name:'Person', //组件名
        setup(){
            // 数据
            let name = "张三"  //注意：这三个都不是响应式的
            let age = 18
            let tel = '15356500590'

            // 方法
            function changeName(){
                name = 'zhang-san'
            }
            function changeAge{
                age += 1
            }
            function showTel(){
                alert(tel)
            }

            // return {name,age} //{a:name, b:age}的简写形式
            return {name, age, changeName, changeAge, showTel}
        }
    }
</script>

<style scoped>
    .person {
        background-color: skyblue;
        box-shadow: 0 0 10px;
        border-radius: 10px;
        padding: 20px;
    }
    button {
        margin: 5px;
        background-color: red;
        box-shadow: 0 0 5px;
        border-radius: 5px;
    }
</style>