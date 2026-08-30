<template>
  <div class="min-h-screen bg-stone-50 text-zinc-950">
    <header class="sticky top-0 z-30 border-b border-zinc-950/10 bg-stone-50/90 backdrop-blur">
      <div class="mx-auto flex max-w-6xl items-center justify-between px-5 py-4 sm:px-8">
        <NuxtLink to="/" class="text-lg font-black tracking-[-0.06em]">Sandip<span class="text-indigo-600">.</span></NuxtLink>
        <nav class="flex items-center gap-1 text-sm font-medium text-zinc-600" aria-label="Main navigation">
          <NuxtLink
            v-for="link in links"
            :key="link.to"
            :to="link.to"
            class="rounded-md px-3 py-2 transition hover:bg-zinc-950 hover:text-white"
            :class="{ 'text-zinc-950': $route.path === link.to }"
          >{{ link.label }}</NuxtLink>
        </nav>
      </div>
    </header>
    <main><slot /></main>
  </div>
</template>

<script setup>
const links = [{ to: '/', label: 'Home' }, { to: '/work', label: 'Work' }, { to: '/about', label: 'About' }, { to: '/contact', label: 'Contact' }]
</script>
