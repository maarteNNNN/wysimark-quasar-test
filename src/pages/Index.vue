<template>
  <q-page class="flex flex-center">
    <img
      alt="Quasar logo"
      src="~assets/quasar-logo-vertical.svg"
      style="width: 200px; height: 200px"
    />
    <Wysimark />
    <q-btn @click="openDialog" label="Open Wysimark" />
    <q-dialog v-model="modal"><Wysimark /></q-dialog>
  </q-page>
</template>

<script>
import Wysimark from "src/components/Wysimark.vue";
import { defineComponent, ref } from "vue";

export default defineComponent({
  components: { Wysimark },
  name: "PageIndex",
  setup() {
    const modal = ref(false);

    return {
      modal,
      openDialog: () => modal.value = !modal.value,
    };
  },
});
</script>
