<template>
  <h4>{{msg}}</h4>
  <button @click="count++">Press Me</button>
  {{count}}
</template>

<script setup="props,{emit}">
import { watchEffect } from "vue";
import { ref } from "vue";
watchEffect(() => console.log(props.msg));

export const count = ref(0);
export default {
  props: {
    msg: String,
  },
  inheritAttrs: false,
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
