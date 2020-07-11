<template>
  <div>
    <input v-model="localMessage" @input="$emit('update:message', localMessage)">
  </div>
</template>

<script>
export default {
  name: "ChildComponent",
  data() {
    return {
      localMessage: this.message
    };
  },
  props: {
    message: {
      type: String,
      required: true
    }
  },
  watch: {
    localMessage(message) {
      this.$emit("update", message);
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
