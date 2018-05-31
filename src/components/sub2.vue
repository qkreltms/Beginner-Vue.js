<template>
    <div>
        sub2
        <button v-on:click= "sendData">click</button>
    </div>
</template>

<script>
export default {
    name: 'sub2',
    methods: {
        sendData: function() {
            eventBus.$emit('testEvent', this.voca)
        }
    },
    data: function() {
        return {
             voca: ["test","test2","test3"]
        }
    }
}
</script>

<style>
</style>
