<template>
  <Wysimark ref="wysimark" v-model="text" style="width: 100%" />
</template>

<script>
import { ref } from "vue";

import Wysimark from "wysimark-vue-3";

export default {
  setup() {
    return {
      text: ref(null),
    };
  },
  components: { Wysimark },
};
</script>
