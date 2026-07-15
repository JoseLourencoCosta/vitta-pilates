<script setup>
import {
  AlignVerticalJustifyCenter,
  Dumbbell,
  Move,
  HeartPulse,
  Scale,
  UserRoundCheck,
} from "lucide-vue-next";

import { benefits } from "../../data/benefits";
import "./Benefits.css";

const icons = {
  AlignVerticalJustifyCenter,
  Dumbbell,
  Move,
  HeartPulse,
  Scale,
  UserRoundCheck,
};
</script>

<template>
  <section class="benefits" id="beneficios">
    <div class="benefits__container">
      <div class="benefits__heading">
        <span>Benefícios</span>

        <h2>Movimento que transforma sua rotina</h2>

        <p>
          O Pilates contribui para uma vida mais ativa, equilibrada e
          confortável, respeitando o ritmo e as necessidades de cada aluno.
        </p>
      </div>

      <div class="benefits__grid">
        <article
          v-for="benefit in benefits"
          :key="benefit.id"
          class="benefits__card"
        >
          <div class="benefits__icon">
            <component
              :is="icons[benefit.icon]"
              :size="28"
              :stroke-width="1.8"
              aria-hidden="true"
            />
          </div>

          <h3>{{ benefit.title }}</h3>

          <p>{{ benefit.description }}</p>
        </article>
      </div>
    </div>
  </section>
</template>
