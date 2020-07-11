<template>
  <child-component :message.sync="message"></child-component>
</template>

<script>
import ChildComponent from "./components/ChildComponent";

export default {
  name: "App",
  components: {
    ChildComponent
  },
  data() {
    return {
      message: "Abhay"
    };
  },
  methods: {
    updateMessage(message) {
      this.message = message;
    }
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
