<template>
    <div>
        sub
<<<<<<< HEAD
        <!-- <table border=1>
            <tr v-for="item in exampleProp" :key="item.e">
                <td>{{item.e}}</td>
=======
        <table border=1>
            <tr v-for="item in voca" v-bind:key= item.e>
                <td>v-model= item.e</td>
>>>>>>> 6f9c49afcdd1d62b185e6270a7bc5187a59179bb
                <td>{{item.k}}</td>
            </tr>
        </table> -->
        <ul>
            <li v-for="item in exampleProp">{{item}}</li>
        </ul>
    </div>
</template>

<script>
import Vue from 'vue'
const eventBus= new Vue()
export { eventBus }


export default {
    name: 'sub1',
     mounted: function() {
    eventBus.$on('testEvent', function(value) {
      this.voca = value
      console.log(this.voca)
    })
  },
    data() {
      return {
        voca: [
            {"e" :"happy1", "k": "행복1"}
        ]
      }  
    },
    computed: {
    }
}
</script>

<style>
</style>
