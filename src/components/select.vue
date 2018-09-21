<template>
    <section class="warp">
        <div class="searchIpt clearFix">
            <select-input :is-show.sync="listShow" :title="title"></select-input>
            <list  v-show="listShow" :data="listData" @changeTitle="titleHandle"></list>
        </div>
    </section>
</template>

<script>
import selectInput from '@/components/selectInput'
import list from '@/components/list'

let ListData=[
    {
        title:'javascript'
    },
    {
        title:'html+css'
    },
    {
        title:'jQuery'
    },
    {
        title:'react'
    },
    {
        title:'node.js'
    }
]
export default {

        components: {
        selectInput,
        list
    },
    data () {
        return {
            listShow:false,
            listData:ListData,
            title:''
        }
    },
    methods: {
        titleHandle(title){
            this.title=title;
        }
    }


}
</script>

<style>

</style>
