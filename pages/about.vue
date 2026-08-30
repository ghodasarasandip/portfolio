<template>
  <section class="section-shell">
    <SectionHeading id="about" label="About" title="An engineer who cares about the details that make software useful." />
    <div class="grid gap-12 lg:grid-cols-[1.25fr_0.75fr]">
      <div class="space-y-5 text-base leading-8 text-zinc-700">
        <p>I’m Sandip, a Senior Software Engineer based in Ahmedabad, India. I enjoy working across the full product surface—from a considered interface to the backend systems that make it dependable.</p><p>Over the last four years, I’ve shipped SaaS products, enterprise workflows, and AI-assisted experiences using Laravel, Vue, React, and Node.js. I’m especially drawn to complex product problems that benefit from a simple, well-reasoned solution.</p><p>When I join a project, I bring pragmatic engineering, clear communication, and a strong sense of ownership.</p>
      </div>
      <div class="rounded-xl border border-zinc-200 bg-white p-6">
        <p class="text-xs font-bold uppercase tracking-[0.16em] text-indigo-700">
          Based in
        </p><p class="mt-3 text-xl font-bold tracking-tight">
          Ahmedabad, India
        </p><div class="my-6 border-t border-zinc-200" /><p class="text-xs font-bold uppercase tracking-[0.16em] text-indigo-700">
          Focus
        </p><p class="mt-3 text-sm leading-6 text-zinc-600">
          Full-stack product development, APIs, SaaS platforms, and AI-enabled workflows.
        </p>
      </div>
    </div>
    <div class="mt-20">
      <SectionHeading id="skills" label="Capabilities" title="A practical, product-minded toolkit." /><div class="grid gap-4 sm:grid-cols-2">
        <div v-for="item in skills" :key="item.title" class="rounded-xl border border-zinc-200 bg-white p-5">
          <h2 class="font-bold">
            {{ item.title }}
          </h2><p class="mt-2 text-sm leading-6 text-zinc-600">
            {{ item.items }}
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
useSeoMeta({ title: 'About · Sandip Ghodasara', description: 'About Sandip Ghodasara, Senior Software Engineer.' })
const skills = [{ title: 'Frontend', items: 'Vue.js, Nuxt, React, Next.js, TypeScript, Tailwind CSS' }, { title: 'Backend', items: 'Laravel, PHP, Node.js, REST APIs, queues, integrations' }, { title: 'Data & infrastructure', items: 'MySQL, PostgreSQL, MongoDB, Redis, Docker, AWS' }, { title: 'Product delivery', items: 'Technical planning, UI implementation, performance, maintainability' }]
</script>
