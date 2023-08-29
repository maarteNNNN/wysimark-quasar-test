<template>
  <q-page class="flex flex-center">
    <wysimark v-model="markdown" :height="320" />
  </q-page>
</template>

<script setup>
import { ref } from "vue";

import wysimark from "@wysimark/vue";

const markdown = ref("");
</script>
