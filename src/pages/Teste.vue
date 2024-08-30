<template>
  <div>
    <h3>
      {{ value }}
    </h3>
    <BtnSave />
  </div>
</template>

<script lang="ts" setup>
import BtnSave from "src/components/BtnSave.vue";
import { ref, computed } from "vue";
function mudar() {
  aux1.value = 13;
}
const aux1 = ref(10);
const aux2 = ref(0);

const value = computed(() => aux1.value + aux2.value);
</script>
