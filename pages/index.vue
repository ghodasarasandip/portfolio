<template>
  <div>
    <section class="mx-auto min-h-[calc(100vh-65px)] max-w-6xl px-5 py-16 sm:px-8 lg:py-24">
      <div>
        <p class="mb-5 inline-flex items-center gap-2 rounded-full border border-indigo-200 bg-indigo-50 px-3 py-1 text-xs font-semibold text-indigo-700">
          <span class="h-1.5 w-1.5 rounded-full bg-indigo-600" /> Available for select opportunities
        </p>
        <p class="mb-4 text-sm font-medium text-zinc-500">
          Hey, I’m
        </p>
        <h1 class="max-w-3xl text-5xl font-black leading-[0.92] tracking-[-0.075em] sm:text-7xl">
          Sandip<br><span class="highlight">Ghodasara</span>
        </h1>
        <p class="mt-8 max-w-xl text-xl font-medium leading-snug tracking-[-0.03em] text-zinc-800 sm:text-2xl">
          I build reliable web products and thoughtful software systems.
        </p>
        <p class="mt-5 max-w-xl text-base leading-7 text-zinc-600">
          Senior Software Engineer specializing in Laravel, Vue, React, and Node.js. I turn complex workflows into clear, scalable products that teams enjoy using.
        </p>
        <div class="mt-7 flex flex-wrap gap-2">
          <span v-for="skill in highlights" :key="skill" class="rounded-md border border-zinc-200 bg-white px-3 py-1.5 text-xs font-medium text-zinc-600">{{ skill }}</span>
        </div>
        <div class="mt-9 flex flex-wrap gap-3">
          <NuxtLink to="/contact" class="button-primary">Let’s work together →</NuxtLink><a
            href="/cv/Sandip_Ghodasara_Int_new.pdf"
            target="_blank"
            rel="noopener"
            class="button-secondary"
          >Resume ↗</a><a
            href="https://github.com/sandipGit2023"
            target="_blank"
            rel="noopener"
            class="button-secondary"
          >GitHub</a><a
            href="https://linkedin.com/in/ghodasara-sandip"
            target="_blank"
            rel="noopener"
            class="button-secondary"
          >LinkedIn</a>
        </div>
      </div>
    </section>
    <section class="section-shell pt-8">
      <SectionHeading id="experience-heading" label="Experience" title="A few places I’ve shipped meaningful work." /><ol class="divide-y divide-zinc-200 border-t border-zinc-200">
        <li v-for="job in experience" :key="job.company" class="grid gap-3 py-7 sm:grid-cols-[150px_1fr] sm:gap-8">
          <p class="text-xs font-semibold text-indigo-700">
            {{ job.period }}
          </p><div>
            <h3 class="font-bold tracking-tight">
              {{ job.role }} <span class="font-normal text-zinc-500">· {{ job.company }}</span>
            </h3><p class="mt-2 max-w-2xl text-sm leading-6 text-zinc-600">
              {{ job.description }}
            </p>
          </div>
        </li>
      </ol>
    </section>
    <section class="section-shell">
      <SectionHeading id="projects-heading" label="Selected work" title="Products made to solve real problems." /><div class="grid gap-4 md:grid-cols-2">
        <article v-for="project in projects" :key="project.name" class="group rounded-xl border border-zinc-200 bg-white p-6 transition hover:-translate-y-1 hover:border-zinc-400 hover:shadow-lg hover:shadow-zinc-950/5">
          <p class="text-xs font-semibold text-indigo-700">
            {{ project.category }}
          </p><h3 class="mt-3 text-xl font-bold tracking-tight">
            {{ project.name }}
          </h3><p class="mt-3 text-sm leading-6 text-zinc-600">
            {{ project.description }}
          </p><div class="mt-5 flex flex-wrap gap-2">
            <span v-for="tech in project.tech" :key="tech" class="rounded bg-zinc-100 px-2 py-1 text-xs text-zinc-600">{{ tech }}</span>
          </div>
        </article>
      </div><NuxtLink to="/work" class="mt-8 inline-flex items-center gap-2 text-sm font-bold hover:text-indigo-700">See all projects →</NuxtLink>
    </section>
    <section class="section-shell">
      <SectionHeading id="stack-heading" label="Stack" title="Tools I use to bring products to life." /><div class="divide-y divide-zinc-200 border-y border-zinc-200">
        <div v-for="row in stack" :key="row.label" class="grid gap-2 py-4 sm:grid-cols-[160px_1fr]">
          <p class="text-xs font-bold uppercase tracking-wider text-indigo-700">
            {{ row.label }}
          </p><p class="text-sm text-zinc-700">
            {{ row.items }}
          </p>
        </div>
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
useSeoMeta({ title: 'Sandip Ghodasara · Senior Software Engineer', description: 'Senior Software Engineer specializing in Laravel, Vue, React, and Node.js.' })
const highlights = ['Laravel', 'Vue.js', 'React', 'Node.js', 'Product engineering']
const experience = [{ period: '2024 — Present', role: 'Freelance Software Engineer', company: 'Independent', description: 'Partnering with teams to design, build, and improve production web applications.' }, { period: '2024', role: 'Senior Software Engineer', company: 'Intelivita', description: 'Delivered scalable web experiences and guided technical execution across product work.' }, { period: '2022 — 2024', role: 'Senior Software Engineer', company: 'Bytes Technolab', description: 'Built dependable full-stack products, integrations, and APIs for client teams.' }, { period: '2021 — 2022', role: 'Junior Web Developer', company: 'WebOccult Technologies', description: 'Started my engineering career shipping web features and backend services.' }]
const projects = [{ name: 'Trady', category: 'SaaS platform', description: 'A service-business platform for instant websites, booking, payments, and job management.', tech: ['Laravel', 'Next.js', 'Node.js', 'MySQL'] }, { name: 'Jib', category: 'AI product', description: 'A no-code SaaS creation experience powered by natural-language workflows and integrations.', tech: ['Laravel', 'Nuxt', 'MySQL'] }, { name: 'AEIS', category: 'Enterprise software', description: 'Document management for critical infrastructure teams, designed for secure collaboration.', tech: ['Laravel', 'React', 'PostgreSQL'] }, { name: 'Eatcard', category: 'Hospitality technology', description: 'An integrated POS, ordering, reservations, kiosk, and delivery platform.', tech: ['Laravel', 'Vue', 'MySQL'] }]
const stack = [{ label: 'Frontend', items: 'Vue.js · Nuxt · React · Next.js · TypeScript · Tailwind CSS' }, { label: 'Backend', items: 'Laravel · PHP · Node.js · REST APIs · Queue workers' }, { label: 'Data', items: 'MySQL · PostgreSQL · MongoDB · Redis' }, { label: 'Tooling', items: 'Git · Docker · AWS · CI/CD · Figma' }]
</script>
