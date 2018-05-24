<template>
    <div>
        sub2
        <button v-on:click= "sendData">click</button>
    </div>
</template>

<script>
import { eventBus } from '../App.vue'
export default {
    name: 'sub2',
    methods: {
        sendData: function() {
            eventBus.$emit('testEvent', 100)
        }
    }
}
</script>

<style>
</style>
