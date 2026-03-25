<script setup>
const problems = [
  {
    icon: `<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 2.69l5.66 5.66a8 8 0 1 1-11.31 0z"/></svg>`,
    title: 'Debit redus sau inexistent',
    causes: 'Diverse blocaje, cum ar fi acumularea de tartru în conducte sau filtrele infuzorului înfundate.',
    solutions: 'Curățarea și detartrarea periodică a espressorului.',
  },
  {
    icon: `<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="3"/><path d="M19.4 15a1.65 1.65 0 0 0 .33 1.82l.06.06a2 2 0 0 1 0 2.83 2 2 0 0 1-2.83 0l-.06-.06a1.65 1.65 0 0 0-1.82-.33 1.65 1.65 0 0 0-1 1.51V21a2 2 0 0 1-2 2 2 2 0 0 1-2-2v-.09A1.65 1.65 0 0 0 9 19.4a1.65 1.65 0 0 0-1.82.33l-.06.06a2 2 0 0 1-2.83 0 2 2 0 0 1 0-2.83l.06-.06A1.65 1.65 0 0 0 4.68 15a1.65 1.65 0 0 0-1.51-1H3a2 2 0 0 1-2-2 2 2 0 0 1 2-2h.09A1.65 1.65 0 0 0 4.6 9a1.65 1.65 0 0 0-.33-1.82l-.06-.06a2 2 0 0 1 0-2.83 2 2 0 0 1 2.83 0l.06.06A1.65 1.65 0 0 0 9 4.68a1.65 1.65 0 0 0 1-1.51V3a2 2 0 0 1 2-2 2 2 0 0 1 2 2v.09a1.65 1.65 0 0 0 1 1.51 1.65 1.65 0 0 0 1.82-.33l.06-.06a2 2 0 0 1 2.83 0 2 2 0 0 1 0 2.83l-.06.06a1.65 1.65 0 0 0-.33 1.82V9a1.65 1.65 0 0 0 1.51 1H21a2 2 0 0 1 2 2 2 2 0 0 1-2 2h-.09a1.65 1.65 0 0 0-1.51 1z"/></svg>`,
    title: 'Cafea prea slabă sau prea tare',
    causes: 'Setări incorecte ale cantității de cafea sau gradului de măcinare, acumulare de tartru în sistemul de distribuție a apei.',
    solutions: 'Ajustarea setărilor de măcinare, curățarea și reglarea espressorului.',
  },
  {
    icon: `<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="11" cy="11" r="8"/><line x1="21" y1="21" x2="16.65" y2="16.65"/></svg>`,
    title: 'Apelează după apă sau nu se oprește automat',
    causes: 'Probleme cu senzorii sau valvele de control al apei.',
    solutions: 'Verificarea senzorilor și înlocuirea acestora dacă este necesar, curățarea sau înlocuirea valvelor.',
  },
  {
    icon: `<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polygon points="13 2 3 14 12 14 11 22 21 10 12 10 13 2"/></svg>`,
    title: 'Zgomote neobișnuite',
    causes: 'Componente uzate, blocaje sau deteriorări ale mecanismului intern.',
    solutions: 'Verificarea vizuală a componentelor, înlocuirea celor uzate sau deteriorate, efectuarea de mentenanță periodică.',
  },
  {
    icon: `<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 2.69l5.66 5.66a8 8 0 1 1-11.31 0z"/></svg>`,
    title: 'Infiltrații de apă sau scurgeri',
    causes: 'Garnituri sau etanșări deteriorate, conducte sau rezervoare sparte.',
    solutions: 'Înlocuirea garniturilor, repararea sau înlocuirea componentelor afectate.',
  },
  {
    icon: `<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M14.7 6.3a1 1 0 0 0 0 1.4l1.6 1.6a1 1 0 0 0 1.4 0l3.77-3.77a6 6 0 0 1-7.94 7.94l-6.91 6.91a2.12 2.12 0 0 1-3-3l6.91-6.91a6 6 0 0 1 7.94-7.94l-3.76 3.76z"/></svg>`,
    title: 'Probleme cu aburul sau spumarea laptelui',
    causes: 'Probleme cu sistemul de abur, duza înfundată, acumulare de lapte uscat.',
    solutions: 'Curățarea duzei de abur, efectuarea de cicluri de curățare a sistemului de abur, înlocuirea sau repararea componentelor defecte.',
  },
  {
    icon: `<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polygon points="13 2 3 14 12 14 11 22 21 10 12 10 13 2"/></svg>`,
    title: 'Probleme electrice sau defecțiuni ale electronicii',
    causes: 'Întreruperi în alimentarea cu curent, probleme cu placa de control, componente electrice defecte.',
    solutions: 'Verificarea conexiunilor electrice, înlocuirea sau repararea componentelor electronice defecte.',
  },
]
</script>

<template>
  <section id="probleme" class="section section--alt">
    <div class="container">
      <div class="section__header" data-aos="fade-up">
        <h2 class="section__title">Defecțiuni frecvente la espressoare</h2>
        <p class="section__subtitle">
          Defecțiunile la un espressor de cafea pot varia în funcție de marcă,
          model și frecvența utilizării. Iată cele mai frecvente probleme
          întâlnite la espressoare:
        </p>
      </div>

      <div class="services__grid">
        <div
          v-for="(problem, index) in problems"
          :key="problem.title"
          class="service-card"
          data-aos="fade-up"
          :data-aos-delay="index * 100"
        >
          <div class="service-card__icon" v-html="problem.icon"></div>
          <h3 class="service-card__title">{{ problem.title }}</h3>
          <p class="service-card__description">
            <strong>Cauze posibile:</strong> {{ problem.causes }}
          </p>
          <p class="service-card__description" style="margin-top: 0.5rem;">
            <strong>Soluții:</strong> {{ problem.solutions }}
          </p>
        </div>
      </div>
    </div>
  </section>
</template>
