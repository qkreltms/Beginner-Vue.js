<template>
  <div id="app">
    <sub1 :exampleProp= voca v-model= voca />
    <sub2></sub2>
  </div>
</template>

<script>
import sub1 from "./components/sub1"
import sub2 from "./components/sub2"
import Vue from 'vue'

const eventBus= new Vue()
export { eventBus }
//props로 JSON보내기 시험중
export default {
  eventBus,
  name: "App",
  mounted: function() {
    console.log(this.voca)
    eventBus.$on('testEvent', function(value) {
      this.voca = value
      console.log(this.voca)
    })
  },
  components: {
    sub1,
    sub2
  },
  data: function () {
    return {
      message: '',
      voca: [
        {"e" :"happy1", "k": "행복1"}
      ]
    }
  }
};
</script>