<template>
    <div>
        sub
        <!-- <table border=1>
            <tr v-for="item in exampleProp" :key="item.e">
                <td>{{item.e}}</td>
                <td>{{item.k}}</td>
            </tr>
        </table> -->
        <button v-on:click="test">test</button>

    </div>
</template>

<script>
import Vue from 'vue'

export default {
    name: 'sub1',
     mounted() {
        eventBus.$on('testEvent', function(value) {
            console.log(this.voca1) //window에 속해있지 않기때문에 언디파인드 출력
            this.voca1 = value
    })
  },
    data() {
      return {
        voca1: "test"
      }  
    },
    methods: {
        test: function() {
            console.log(this.voca1)
        }
    }
}
</script>

<style>
</style>
