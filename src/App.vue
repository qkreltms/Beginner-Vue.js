<template>
  <div id="app">
    <sub1 :exampleProp=voca />
  </div>
</template>

<script>
import sub1 from "./components/sub1";

export default {
  name: "App",
  components: {
    'sub1': sub1
  },
  data: function () {
    return {
      message: '',
      voca: [
        {"e" :"happy1", "k": "행복1"},
        {"e" :"happy2", "k": "행복2"},
        {"e" :"happy3", "k": "행복3"}
      ]
    }
  }
};
</script>