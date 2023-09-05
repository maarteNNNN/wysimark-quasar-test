<template>
  <q-page class="flex column q-gutter-md flex-center">
    <div>
      <h5 class="q-ma-sm">V-Model example</h5>
      <wysimark v-model="markdown" :height="320" />
    </div>
    <div>
      <h5 class="q-ma-sm">
        Checklist example (clicking a checkbox will log any @update:model-value
        event in the console with the value)
      </h5>
      <wysimark
        :model-value="checklistExample"
        @update:model-value="log"
        :height="320"
      />
    </div>
  </q-page>
</template>

<script setup>
import { ref } from "vue";

import wysimark from "@wysimark/vue";

const markdown = ref("");
const checklistExample = ref(
  "- [ ] Test for Sunny \n - [x] Test for Sunny2 \n - [ ] Test for Sunny3"
);

const log = console.log;
</script>
