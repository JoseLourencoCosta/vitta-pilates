<script setup>
import { ArrowRight, MessageCircle } from "lucide-vue-next";
import "./CTA.css";

const whatsappLink =
  "https://wa.me/5521968413603?text=Olá!%20Gostaria%20de%20saber%20mais%20sobre%20as%20aulas%20no%20Studio%20Vitta%20Pilates.";
</script>

<template>
  <section class="cta" id="contato">
    <div class="cta__container">
      <div class="cta__content">
        <span class="cta__eyebrow">Seu próximo passo começa aqui</span>

        <h2>Cuide do seu corpo com movimento, atenção e propósito.</h2>

        <p>
          Agende uma conversa com o Studio Vitta Pilates e descubra como as
          aulas podem contribuir para sua saúde, mobilidade e qualidade de vida.
        </p>
      </div>

      <a
        class="cta__button"
        :href="whatsappLink"
        target="_blank"
        rel="noopener noreferrer"
        aria-label="Falar com o Studio Vitta Pilates pelo WhatsApp"
      >
        <MessageCircle :size="21" aria-hidden="true" />
        <span>Agendar pelo WhatsApp</span>
        <ArrowRight :size="19" aria-hidden="true" />
      </a>
    </div>
  </section>
</template>
