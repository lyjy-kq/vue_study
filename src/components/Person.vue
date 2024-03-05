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
        data(){
            return {
                name:'张三',
                age:18,
                tel:'15356500590'
            }
        },
        methods:{
            showTel(){
                alert(this.tel)
            },
            changeName(){
                this.name='Zhang San'
            },
            changeAge(){
                this.age+=1
            }
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