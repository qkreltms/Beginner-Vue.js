<template>
  <div id="app">
    <sub1 :exampleProp= voca />
    <sub2></sub2>
  </div>
</template>

<script>
import sub1 from "./components/sub1"
import sub2 from "./components/sub2"
import Vue from 'vue'

window.eventBus= new Vue()

//props로 JSON보내기 시험중
export default {
  name: "App",
    data: function () {
    return {
      message: '',
      voca: ['a']
    }
  },
  mounted() {
    eventBus.$on('testEvent', function(value) {
      this.voca = value
      console.log(this.voca)
    })
},
  components: {
    sub1,
    sub2
  }
};
</script>
