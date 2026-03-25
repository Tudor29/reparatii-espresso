<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const isMobileMenuOpen = ref(false)
const isScrolled = ref(false)

const toggleMenu = () => {
  isMobileMenuOpen.value = !isMobileMenuOpen.value
}

const closeMenu = () => {
  isMobileMenuOpen.value = false
}

const handleScroll = () => {
  isScrolled.value = window.scrollY > 50
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll, { passive: true })
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>

<template>
  <header class="navbar" :class="{ 'navbar--scrolled': isScrolled }">
    <div class="container navbar__inner">
      <a href="#" class="navbar__brand">
        <img src="/logo.png" alt="Abil Service" class="navbar__logo" />
      </a>

      <nav
        class="navbar__links"
        :class="{ 'navbar__links--open': isMobileMenuOpen }"
      >
        <a href="#probleme" @click="closeMenu">Defecțiuni</a>
        <a href="#proces" @click="closeMenu">Cum funcționează</a>
        <a href="#despre" @click="closeMenu">Despre noi</a>
        <a href="#contact" @click="closeMenu">Contact</a>
        <a
          href="tel:0745048258"
          class="btn btn--primary navbar__cta"
          @click="closeMenu"
        >
          0745 048 258
        </a>
      </nav>

      <button
        class="navbar__hamburger"
        :class="{ 'navbar__hamburger--active': isMobileMenuOpen }"
        @click="toggleMenu"
        aria-label="Deschide meniul de navigare"
      >
        <span></span>
        <span></span>
        <span></span>
      </button>
    </div>
  </header>
</template>
