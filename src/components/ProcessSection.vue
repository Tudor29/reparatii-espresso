<script setup>
const steps = [
  {
    number: '01',
    title: 'Apel telefonic sau online',
    description: 'Contactați-ne pentru a ne descrie problema espressorului dumneavoastră.',
  },
  {
    number: '02',
    title: 'Diagnosticare rapidă',
    description: 'Identificăm cauza defecțiunii și vă oferim un diagnostic clar.',
  },
  {
    number: '03',
    title: 'Reparare eficientă',
    description: 'Intervenim rapid cu piese de calitate pentru o reparație de durată.',
  },
  {
    number: '04',
    title: 'Finalizare și garanție',
    description: 'Predăm echipamentul funcțional, cu garanție extinsă de 6 luni.',
  },
]
</script>

<template>
  <section id="proces" class="section section--bg-image section--bg-light" style="background-image: url('/images/coffee.jpg')">
    <div class="container">
      <div class="section__header" data-aos="fade-up">
        <h2 class="section__title">Cum puteți beneficia de serviciile noastre</h2>
        <p class="section__subtitle">
          Procesul nostru este simplu și transparent, de la primul apel până la
          finalizarea reparației.
        </p>
      </div>

      <div class="process__grid">
        <div
          v-for="(step, index) in steps"
          :key="step.number"
          class="process-card"
          data-aos="fade-up"
          :data-aos-delay="index * 100"
        >
          <div class="process-card__number">{{ step.number }}</div>
          <h3 class="process-card__title">{{ step.title }}</h3>
          <p class="process-card__description">{{ step.description }}</p>
        </div>
      </div>
    </div>
  </section>
</template>
