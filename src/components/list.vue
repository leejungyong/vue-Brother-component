<template>
    <ul class="list">
        <li 
        v-for="(item,index) in data" 
        :key='index'
        @click="getTitleHandle(item.title)"
        >{{item.title}}</li>
        <!-- <li>html5+css3</li>
        <li>javascript</li>
        <li>angular</li>
        <li>react</li>
        <li>vue</li>
        <li>jquery</li>
         <li>node.js</li> -->
    </ul>
</template>

<script>
export default {
    props:['data'],
    data () {
        return {
            
        }
    },
    methods: {
        getTitleHandle(title){
            this.$emit('changeTitle',title); //触发父组件定义的函数
        }
    }

}
</script>

<style>

</style>
