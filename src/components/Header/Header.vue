<script setup>
import { ref } from "vue";
import { Menu, X } from "lucide-vue-next";

import "./Header.css";
import logoVittaPilates from "../../assets/logo/logo-vitta-horizontal.webp";

const isMobileMenuOpen = ref(false);

const toggleMobileMenu = () => {
  isMobileMenuOpen.value = !isMobileMenuOpen.value;
};

const closeMobileMenu = () => {
  isMobileMenuOpen.value = false;
};
</script>

<template>
  <header class="header">
    <div class="header__container">
      <a
        href="#inicio"
        class="header__brand"
        aria-label="Studio Vitta Pilates - Página inicial"
        @click="closeMobileMenu"
      >
        <img
          :src="logoVittaPilates"
          alt="Logo Vitta Pilates"
          class="header__logo"
        />
      </a>

      <nav class="header__nav" aria-label="Navegação principal">
        <a href="#inicio">Início</a>
        <a href="#especialidades">Especialidades</a>
        <a href="#beneficios">Benefícios</a>
        <a href="#sobre">Sobre</a>
        <a href="#depoimentos">Depoimentos</a>
        <a href="#contato">Contato</a>
      </nav>

      <a
        href="https://wa.me/5521968413603"
        class="header__button"
        target="_blank"
        rel="noopener noreferrer"
      >
        Agende uma aula
      </a>

      <button
        class="header__menu-button"
        type="button"
        :aria-expanded="isMobileMenuOpen"
        aria-controls="mobile-navigation"
        aria-label="Abrir menu de navegação"
        @click="toggleMobileMenu"
      >
        <X v-if="isMobileMenuOpen" :size="26" />
        <Menu v-else :size="26" />
      </button>
    </div>

    <nav
      id="mobile-navigation"
      class="header__mobile-nav"
      :class="{ 'header__mobile-nav--open': isMobileMenuOpen }"
      aria-label="Navegação mobile"
    >
      <a href="#inicio" @click="closeMobileMenu">Início</a>
      <a href="#especialidades" @click="closeMobileMenu"> Especialidades </a>
      <a href="#beneficios" @click="closeMobileMenu"> Benefícios </a>
      <a href="#sobre" @click="closeMobileMenu"> Sobre </a>
      <a href="#depoimentos" @click="closeMobileMenu"> Depoimentos </a>
      <a href="#contato" @click="closeMobileMenu"> Contato </a>

      <a
        href="https://wa.me/5521968413603"
        class="header__mobile-button"
        target="_blank"
        rel="noopener noreferrer"
        @click="closeMobileMenu"
      >
        Agende uma aula
      </a>
    </nav>
  </header>
</template>
