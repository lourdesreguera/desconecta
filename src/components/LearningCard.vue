<script setup>
defineProps({
  item: Object,
  index: Number
})
</script>

<template>
  <div class="card border-white py-2 h-100">
    <div class="card-body">
      <p class="fs-2 fw-bold text-primary text-center">{{ index + 1 }}</p>
      <p v-html="item.html" class="text-center">
      </p>
    </div>
    <img class="card-img-bottom" :src="item.image" :alt="item.alt" width="300">
  </div>
</template>
