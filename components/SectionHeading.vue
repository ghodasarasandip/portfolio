<template>
  <div class="mb-8">
    <p class="text-xs font-bold uppercase tracking-[0.16em] text-indigo-700">
      {{ label }}
    </p>
    <h2 :id="id" class="mt-3 max-w-2xl text-3xl font-black tracking-[-0.05em] sm:text-4xl">
      {{ title }}
    </h2>
  </div>
</template>

<script setup>
defineProps({ id: { type: String, required: true }, label: { type: String, required: true }, title: { type: String, required: true } })
</script>
