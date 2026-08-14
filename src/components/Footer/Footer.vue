<script setup>
import { Instagram, MapPin, MessageCircle } from "lucide-vue-next";

import logoVittaPilates from "../../assets/logo/logo-vitta-vertical.png";
import "./Footer.css";

const currentYear = new Date().getFullYear();

const whatsappLink =
  "https://wa.me/5521968413603?text=Olá!%20Gostaria%20de%20saber%20mais%20sobre%20as%20aulas%20no%20Studio%20Vitta%20Pilates.";

const instagramLink = "https://www.instagram.com/vitta_pilates23/";

const mapsLink =
  "https://www.google.com/maps/search/?api=1&query=Rua+Bahia+143+sala+5+Nogueira+Petrópolis+RJ";
</script>

<template>
  <footer class="footer">
    <div class="footer__container">
      <div class="footer__brand">
        <a
          href="#inicio"
          class="footer__logo-link"
          aria-label="Voltar ao início da página"
        >
          <span class="footer__logo-wrapper">
            <img
              :src="logoVittaPilates"
              alt="Studio Vitta Pilates"
              class="footer__logo"
            />
          </span>
        </a>

        <strong>Studio Vitta Pilates</strong>

        <p>
          Movimento, cuidado e qualidade de vida com atendimento personalizado
          em Nogueira, Petrópolis.
        </p>
      </div>

      <div class="footer__contact">
        <span class="footer__eyebrow">Contato</span>

        <div class="footer__links">
          <a
            :href="whatsappLink"
            target="_blank"
            rel="noopener noreferrer"
            aria-label="Falar com o Studio Vitta Pilates pelo WhatsApp"
          >
            <MessageCircle :size="19" aria-hidden="true" />
            <span>WhatsApp</span>
          </a>

          <a
            :href="instagramLink"
            target="_blank"
            rel="noopener noreferrer"
            aria-label="Visitar o Instagram do Studio Vitta Pilates"
          >
            <Instagram :size="19" aria-hidden="true" />
            <span>Instagram</span>
          </a>

          <a
            :href="mapsLink"
            target="_blank"
            rel="noopener noreferrer"
            aria-label="Abrir a localização do Studio Vitta Pilates no Google Maps"
          >
            <MapPin :size="19" aria-hidden="true" />

            <span>
              Rua Bahia, 143, sala 5
              <small>Nogueira, Petrópolis - RJ</small>
            </span>
          </a>
        </div>
      </div>
    </div>

    <div class="footer__bottom">
      <span class="footer__location">
        <MapPin :size="15" aria-hidden="true" />
        Nogueira • Petrópolis • RJ
      </span>

      <span>
        © {{ currentYear }} Studio Vitta Pilates. Todos os direitos reservados.
      </span>
    </div>
  </footer>
</template>
