<template>
  <div>
    <!-- <app-header v-bind:"프롭스 속성의 이름"="상위 컴포넌트의 데이터 이름"></app-header> -->
    <app-header v-bind:propsdata="str" v-on:renew="renewString"> </app-header>
  </div>
</template>
<script>
import AppHeader from "./components/AppHeader.vue";

export default {
  data: function () {
    return {
      str: "header",
    };
  },
  components: {
    "app-header": AppHeader,
  },
  methods: {
    renewString: function () {
      this.str = "hi";
    },
  },
};
</script>
