<template>
  <div class="min-h-screen bg-stone-50 text-zinc-950">
    <header class="sticky top-0 z-30 border-b border-zinc-950/10 bg-stone-50/90 backdrop-blur">
      <div class="mx-auto max-w-6xl px-5 py-4 sm:px-8">
        <div class="flex items-center justify-between gap-4">
          <NuxtLink to="/" class="text-lg font-black tracking-[-0.06em]">Sandip<span class="text-indigo-600">.</span></NuxtLink>

          <button
            type="button"
            class="inline-flex h-10 w-10 items-center justify-center rounded-md border border-zinc-200 bg-white text-zinc-950 transition hover:border-zinc-950 md:hidden"
            aria-label="Toggle navigation"
            aria-expanded="false"
            @click="isMenuOpen = !isMenuOpen"
          >
            <span class="sr-only">Open menu</span>
            <span class="flex flex-col gap-1.5">
              <span class="block h-0.5 w-5 rounded-full bg-current" />
              <span class="block h-0.5 w-5 rounded-full bg-current" />
              <span class="block h-0.5 w-5 rounded-full bg-current" />
            </span>
          </button>

          <nav class="hidden items-center gap-1 text-sm font-medium text-zinc-600 md:flex" aria-label="Main navigation">
            <NuxtLink
              v-for="link in links"
              :key="link.to"
              :to="link.to"
              class="rounded-md px-3 py-2 transition hover:bg-zinc-950 hover:text-white"
              :class="route.path === link.to ? 'bg-zinc-950 text-white' : 'text-zinc-600'"
            >{{ link.label }}</NuxtLink>
          </nav>
        </div>

        <nav
          v-if="isMenuOpen"
          class="mt-4 flex flex-col gap-2 rounded-xl border border-zinc-200 bg-white p-2 text-sm font-medium text-zinc-600 md:hidden"
          aria-label="Mobile navigation"
        >
          <NuxtLink
            v-for="link in links"
            :key="link.to"
            :to="link.to"
            class="rounded-md px-3 py-2.5 transition"
            :class="route.path === link.to ? 'bg-zinc-950 text-white' : 'hover:bg-zinc-100 hover:text-zinc-950'"
            @click="isMenuOpen = false"
          >{{ link.label }}</NuxtLink>
        </nav>
      </div>
    </header>
    <main><slot /></main>
  </div>
</template>

<script setup>
const route = useRoute()
const isMenuOpen = ref(false)

watch(() => route.path, () => {
  isMenuOpen.value = false
})

const links = [{ to: '/', label: 'Home' }, { to: '/work', label: 'Work' }, { to: '/about', label: 'About' }, { to: '/contact', label: 'Contact' }]
</script>
