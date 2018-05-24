<template>
    <div>
        sub2
        <button v-model= voca v-on:click= "sendData">click</button>
    </div>
</template>

<script>
import { eventBus } from '../App.vue'
export default {
    name: 'sub2',
    methods: {
        sendData: function() {
            eventBus.$emit('testEvent', this.voca)
        }
    },
    data: function() {
        return {
             voca: [
                {"e" :"happy1", "k": "행복1"},
                {"e" :"happy2", "k": "행복2"},
                {"e" :"happy3", "k": "행복3"}
      ]
        }
    }
}
</script>

<style>
</style>
