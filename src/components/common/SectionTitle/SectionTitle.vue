<script setup>
import "./SectionTitle.css";

defineProps({
  eyebrow: {
    type: String,
    required: true,
  },
  title: {
    type: String,
    required: true,
  },
  description: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <div class="section-title">
    <span class="section-title__eyebrow">
      {{ eyebrow }}
    </span>

    <h2 class="section-title__heading">
      {{ title }}
    </h2>

    <p class="section-title__description">
      {{ description }}
    </p>
  </div>
</template>
