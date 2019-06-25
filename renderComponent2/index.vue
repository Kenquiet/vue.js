<template>
    <div>
        <async-load-comp
            v-for="comp in comps"
            :app="comp"
            :prop="prop"
        ></async-load-comp>
    </div>
</template>
<script>
    import asyncLoadComp from './dir/asyncLoadComp.vue'
    export default {
        components: {
            asyncLoadComp
        },
        data () {
            return {
                comps: ['comp1', 'comp2'],
                prop: {name: '张三'}
            }
        }
    }
</script>
<style></style>
