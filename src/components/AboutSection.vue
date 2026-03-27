<script setup>
const reasons = [
  {
    title: 'Promptitudine și Răspuns Rapid',
    description: 'Rezolvăm problemele rapid, pentru a minimiza inconveniențele.',
  },
  {
    title: 'Echipa Experților',
    description: 'Tehnicienii noștri sunt bine instruiți și au o vastă experiență în domeniu, de 14 ani.',
  },
  {
    title: 'Onestitate și Transparență',
    description: 'Primești un diagnostic clar și o estimare a costurilor înainte de a începe reparația.',
  },
  {
    title: 'Garanție de Satisfacție',
    description: 'Suntem mândri de serviciile noastre și oferim o garanție extinsă la 6 luni pentru a asigura satisfacția completă a clienților noștri.',
  },
]
</script>

<template>
  <section id="despre" class="section section--alt">
    <div class="container">
      <div class="section__header" data-aos="fade-up">
        <h2 class="section__title">Echipa Abil Service</h2>
        <p class="section__subtitle">
          La Abil Service, suntem dedicați aducerii electrocasnicelor tale la
          viață prin servicii de reparații de încredere. Indiferent de marca sau
          modelul aparatului tău, echipa noastră de tehnicieni experimentați este
          pregătită să ofere soluții rapide și eficiente pentru a restabili
          funcționarea normală a echipamentului tău casnic.
        </p>
      </div>

      <div class="about__image" data-aos="fade-up">
        <img src="/images/aparat.png" alt="Reparații espressoare de cafea" />
      </div>

      <div class="about__grid">
        <div
          v-for="(reason, index) in reasons"
          :key="reason.title"
          class="about-card"
          data-aos="fade-up"
          :data-aos-delay="index * 100"
        >
          <h3 class="about-card__title">{{ reason.title }}</h3>
          <p class="about-card__description">{{ reason.description }}</p>
        </div>
      </div>

      <div class="about__cta" data-aos="fade-up">
        <p>
          Alege Abil Service pentru reparații de încredere și eficiente!
          Sună-ne astăzi și redescoperă confortul în locuința ta.
        </p>
        <a href="#contact" class="btn btn--primary">Contactează-ne</a>
      </div>
    </div>
  </section>
</template>
