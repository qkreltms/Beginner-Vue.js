<template>
    <div>
        sub
        <table border=1>
            <tr v-for="item in voca" v-bind:key= item.e>
                <td>v-model= item.e</td>
                <td>{{item.k}}</td>
            </tr>
        </table>
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
