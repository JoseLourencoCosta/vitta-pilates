<script setup>
import './Hero.css'
</script>

<template>
  <section class="hero" id="inicio">
    <div class="hero__container">
      <div class="hero__content">
        <span class="hero__tag">Studio Vitta Pilates • Nogueira, Petrópolis</span>

        <h1>Pilates para cuidar do corpo com equilíbrio e movimento</h1>

        <p>
          Atendimento com Adriana Lima, unindo Pilates clínico, clássico,
          contemporâneo e funcional em um espaço pensado para seu bem-estar.
        </p>

        <div class="hero__actions">
          <a
            href="https://wa.me/5521968413603"
            class="hero__button hero__button--primary"
            target="_blank"
            rel="noopener noreferrer"
          >
            Agende uma aula
          </a>

          <a
            href="https://www.google.com/maps/search/?api=1&query=Rua%20Bahia%20143%20sala%205%20Nogueira%20Petr%C3%B3polis"
            class="hero__button hero__button--secondary"
            target="_blank"
            rel="noopener noreferrer"
          >
            Ver localização
          </a>
        </div>
      </div>

      <div class="hero__visual" aria-hidden="true">
        <div class="hero__card">
          <span>Pilates clínico</span>
          <strong>Clássico • Contemporâneo • Funcional</strong>
        </div>
      </div>
    </div>
  </section>
</template>