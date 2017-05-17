<template>
    <div class="pa4 content">
        <h1>Hello, World!</h1>
        {{ counter }}
        <br><br>
        <button @click="increment">Increment</button>
        <button @click="decrement">Decrement</button>
    </div>
</template>

<script>
    import {mapState,mapMutations} from 'vuex'
    export default {
        computed: {
            ...mapState({
                counter: state => state.counter
            })
        },
        methods: {
            ...mapMutations([
                'increment',
                'decrement'
            ])
        }
    }
</script>

<style lang="scss">
    .content {
        text-align: center;
    }
</style>