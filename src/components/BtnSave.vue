<template>
  <q-btn color="green" label="Navegar" @click="toRouter" />
</template>
<script lang="ts" setup>
import { useRouter } from "vue-router";


defineOptions({
  name: 'BtnSave'
})
const { push } = useRouter();
const props = defineProps({
  rota: {
    type: String,
    default: "home",
  },
});

function toRouter() {
  push({ name: props.rota });
}
</script>
