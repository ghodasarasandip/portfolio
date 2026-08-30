<template>
  <div>
    <section class="section-shell">
      <SectionHeading id="work" label="Work" title="A closer look at selected product work." />
      <div class="space-y-4">
        <article v-for="project in projects" :key="project.name" class="grid gap-5 rounded-xl border border-zinc-200 bg-white p-6 md:grid-cols-[120px_1fr] md:p-8">
          <p class="text-xs font-bold uppercase tracking-wider text-indigo-700">
            {{ project.period }}
          </p>
          <div>
            <h2 class="text-2xl font-bold tracking-tight">
              {{ project.name }}
            </h2><p class="mt-3 max-w-2xl leading-7 text-zinc-600">
              {{ project.description }}
            </p><div class="mt-5 flex flex-wrap gap-2">
              <span v-for="tech in project.tech" :key="tech" class="rounded-md bg-zinc-100 px-2.5 py-1 text-xs font-medium text-zinc-600">{{ tech }}</span>
            </div>
          </div>
        </article>
      </div>
    </section>

    <section class="border-t border-zinc-200 bg-zinc-950 text-white">
      <div class="section-shell py-20">
        <p class="text-sm font-semibold text-indigo-300">
          Open to interesting problems
        </p><h2 class="mt-3 max-w-2xl text-4xl font-black tracking-[-0.06em] sm:text-5xl">
          Have something worth building?
        </h2><p class="mt-5 max-w-xl leading-7 text-zinc-400">
          Let’s talk about your product, your team, and how I can help.
        </p><NuxtLink to="/contact" class="mt-8 inline-flex rounded-md bg-white px-4 py-2.5 text-sm font-bold text-zinc-950 transition hover:bg-indigo-200">Get in touch →</NuxtLink>
      </div>
    </section>
  </div>
</template>

<script setup>
useSeoMeta({ title: 'Work · Sandip Ghodasara', description: 'Selected projects by Sandip Ghodasara.' })
const projects = [{ period: '2021 — 2023', name: 'Trady', description: 'A product for service professionals to create websites, take bookings, receive payments, and manage their jobs from one place.', tech: ['Laravel', 'Next.js', 'Node.js', 'MySQL'] }, { period: '2022 — 2024', name: 'Jib', description: 'An AI-powered superapp that helps people turn plain-language prompts into no-code SaaS workflows.', tech: ['Laravel', 'Nuxt', 'MySQL'] }, { period: '2020 — 2022', name: 'AEIS', description: 'Secure, collaborative document management for inspection, engineering, and critical infrastructure projects.', tech: ['Laravel', 'React', 'PostgreSQL'] }, { period: '2023 — 2025', name: 'Eatcard', description: 'A unified hospitality platform for POS, takeaway, kiosks, reservations, delivery, and real-time operations.', tech: ['Laravel', 'Vue', 'MySQL'] }, { period: '2024 — 2025', name: '10/1', description: 'A responsive horse-betting experience combining live odds, race tracking, and analytics across web and mobile.', tech: ['Laravel', 'Vue', 'Node.js'] }, { period: '2024 — 2025', name: 'Walkies', description: 'A dog-centric app enhancing pet care and community engagement.', tech: ['Laravel', 'Nuxt', 'Nest.js'] }, { period: '2024 — 2025', name: 'ostiQ', description: 'A medical application streamlining healthcare services.', tech: ['Laravel', 'Nuxt', 'Node.js'] }]
</script>
