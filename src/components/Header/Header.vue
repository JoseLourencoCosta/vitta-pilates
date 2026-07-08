<script setup>
import './Header.css'
import logoVittaPilates from '../../assets/logo/logo-vitta-pilates.png'
</script>

<template>
  <header class="header">
    <div class="header__container">
      <a href="#" class="header__brand" aria-label="Vitta Pilates - Página inicial">
        <img
          :src="logoVittaPilates"
          alt="Logo Vitta Pilates"
          class="header__logo"
        />
      </a>

      <nav class="header__nav" aria-label="Navegação principal">
        <a href="#inicio">Início</a>
        <a href="#beneficios">Benefícios</a>
        <a href="#sobre">Sobre</a>
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
    </div>
  </header>
</template>