<template>
    <div>
        <component v-for="item in apps" :is="item.app"></component>
    </div>
</template>
<script>
    import Vue from 'vue'
    export default {
        data(){
            return{
                comps:['comp1','comp2'],
                apps:[]
            }
        },
        created() {
            this.comps.forEach( app => {
                this.apps.push({app : require('./dir/${this.app}.vue').default})
            })
        }
    }
</script>
