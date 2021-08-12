<template>
  <div class="bw-wysimark">
    <Wysimark
      ref="wysimark"
      class="bw-wysimark"
      v-model="text"
      style="width: 100%"
    />
  </div>
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

<style scoped>
.bw-wysimark {
  width: 100%;
}
</style>
