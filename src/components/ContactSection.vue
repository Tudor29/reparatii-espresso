<script setup>
const schedule = [
  { day: 'Luni', hours: '08:30 - 16:30' },
  { day: 'Marți', hours: '08:30 - 16:30' },
  { day: 'Miercuri', hours: '08:30 - 16:30' },
  { day: 'Joi', hours: '08:30 - 16:30' },
  { day: 'Vineri', hours: '08:30 - 16:30' },
  { day: 'Sâmbătă', hours: 'Închis' },
  { day: 'Duminică', hours: 'Închis' },
]

const websites = [
  'www.abilservice.ro',
  'www.serviceelectrocasnice.com',
  'www.reparatii-frigidere-brasov.ro',
  'www.repartii-electrocasnice-brasov.ro',
  'www.service-reparatii-electrocasnice.ro',
  'www.reparatii-masini-de-spalat-brasov.ro',
]
</script>

<template>
  <section id="contact" class="section section--bg-image" style="background-image: url('/images/espresso-closeup.png')">
    <div class="container">
      <div class="section__header" data-aos="fade-up">
        <h2 class="section__title">Contactează-ne</h2>
        <p class="section__subtitle">
          Ești gata să îți repari espressorul? Sună-ne direct pentru programare.
        </p>
      </div>

      <div class="contact__columns" data-aos="fade-up">
        <div class="contact__info">
          <div class="contact__info-item">
            <h3>Telefon</h3>
            <p><a href="tel:0745048258" class="contact__link">0745 048 258</a></p>
          </div>
          <div class="contact__info-item">
            <h3>Email</h3>
            <p>
              <a href="mailto:reparatiibrasov@gmail.com" class="contact__link">reparatiibrasov@gmail.com</a><br />
              <a href="mailto:abil_service@yahoo.com" class="contact__link">abil_service@yahoo.com</a>
            </p>
          </div>
          <div class="contact__info-item">
            <h3>Locație</h3>
            <p>Str. Baba Novac 80, Brașov</p>
            <div class="contact__map-links">
              <a href="https://maps.app.goo.gl/AX3KcYbYFNdmofkr5?g_st=aw" target="_blank" rel="noopener" class="contact__link">Google Maps</a>
              <a href="https://waze.com/ul/hu845xjrdn" target="_blank" rel="noopener" class="contact__link">Waze</a>
            </div>
          </div>
          <div class="contact__info-item">
            <h3>Program de lucru</h3>
            <div class="schedule">
              <div
                v-for="item in schedule"
                :key="item.day"
                class="schedule__row"
              >
                <span class="schedule__day">{{ item.day }}</span>
                <span
                  class="schedule__hours"
                  :class="{ 'schedule__hours--closed': item.hours === 'Închis' }"
                >
                  {{ item.hours }}
                </span>
              </div>
            </div>
          </div>
        </div>

        <div class="contact__info">
          <div class="contact__info-item">
            <h3>Site-uri web</h3>
            <p>
              <a
                v-for="site in websites"
                :key="site"
                :href="'https://' + site"
                target="_blank"
                rel="noopener"
                class="contact__link contact__link--block"
              >
                {{ site }}
              </a>
            </p>
          </div>
          <div class="contact__info-item">
            <h3>Facebook</h3>
            <p>
              <a href="https://www.facebook.com/profile.php?id=100037403726090" target="_blank" rel="noopener" class="contact__link">
                Abil Service pe Facebook
              </a>
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
