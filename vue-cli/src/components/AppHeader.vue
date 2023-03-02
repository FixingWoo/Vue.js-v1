<template>
  <div>
    <header>{{ propsdata }}</header>
    <button type="button" v-on:click="sendEvent">send</button>
  </div>
</template>
<script>
export default {
  props: ["propsdata"],
  methods: {
    sendEvent: function () {
      this.$emit("renew");
    },
  },
};
</script>
