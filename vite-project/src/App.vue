<script setup lang="ts">
import img1 from "./assets/1.jpg";
import img2 from "./assets/2.jpg";
import img3 from "./assets/3.jpg";
import { onMounted, ref } from "vue";
const show = ref(false);
onMounted(() => {
  setTimeout(() => {
    show.value = true;
  }, 10000);
});
</script>

<template>
  <div>
    <div v-if="show">
      <img style="display: block; width: 30%" :src="img1" />
      <img style="display: block; width: 30%" :src="img2" />
      <img style="display: block; width: 30%" :src="img3" />
    </div>
  </div>
</template>
