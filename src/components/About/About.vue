<script setup>
import { HeartHandshake, UsersRound, Dumbbell, MapPin } from "lucide-vue-next";

import SectionTitle from "../common/SectionTitle/SectionTitle.vue";
import "./About.css";
</script>

<template>
  <section class="about" id="sobre">
    <div class="about__container">
      <div class="about__visual" aria-hidden="true"></div>

      <div class="about__content">
        <SectionTitle
          eyebrow="Sobre o Studio"
          title="Mais do que Pilates, um cuidado com você"
          description="No Studio Vitta Pilates, acreditamos que cada aluno possui objetivos únicos. Por isso, oferecemos um ambiente acolhedor, atendimento personalizado e acompanhamento cuidadoso para promover saúde, movimento e qualidade de vida."
        />

        <ul class="about__highlights">
          <li>
            <HeartHandshake :size="24" aria-hidden="true" />
            Atendimento individualizado
          </li>

          <li>
            <UsersRound :size="24" aria-hidden="true" />
            Equipe qualificada
          </li>

          <li>
            <Dumbbell :size="24" aria-hidden="true" />
            Equipamentos modernos
          </li>

          <li>
            <MapPin :size="24" aria-hidden="true" />
            Localização em Nogueira, Petrópolis
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>
