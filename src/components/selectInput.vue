<template>
    <div class="clearFix">
        <input
         readonly='readonly'
         class="keyWord"
         @click="showListHandle"  :value="title"> 
         <input type="button" value="Go">
         <span></span>
    </div>
</template>

<script>
export default {
    props:['isShow','title'],
    computed: {
        initShow(){
            return this.isShow;
        }
    },
    methods: {
        showListHandle(){
            this.$emit("update:isShow",!this.isShow)
        }
    }

}
</script>

<style>

</style>
