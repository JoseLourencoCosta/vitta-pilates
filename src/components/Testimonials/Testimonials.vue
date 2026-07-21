<script setup>
import { Star, BadgeCheck } from "lucide-vue-next";

import SectionTitle from "../common/SectionTitle/SectionTitle.vue";
import { testimonials } from "../../data/testimonials";
import "./Testimonials.css";
</script>

<template>
  <section id="depoimentos" class="testimonials">
    <div class="testimonials__container">
      <SectionTitle
        eyebrow="Depoimentos"
        title="A experiência de quem pratica Pilates conosco"
        description="Avaliações reais compartilhadas por alunos do Studio Vitta Pilates no Google."
      />

      <div
        class="testimonials__summary"
        aria-label="Avaliação 5 de 5 no Google, baseada em mais de 35 avaliações"
      >
        <div class="testimonials__score">
          <strong>5,0</strong>

          <div class="testimonials__summary-stars" aria-hidden="true">
            <Star
              v-for="star in 5"
              :key="star"
              :size="19"
              :stroke-width="1.8"
              fill="currentColor"
            />
          </div>
        </div>

        <div class="testimonials__summary-content">
          <div class="testimonials__summary-title">
            <BadgeCheck :size="20" aria-hidden="true" />
            <strong>Avaliação média no Google</strong>
          </div>

          <span>Mais de 35 avaliações reais</span>
        </div>
      </div>

      <div class="testimonials__grid">
        <article
          v-for="testimonial in testimonials"
          :key="testimonial.id"
          class="testimonials__card"
          :class="{
            'testimonials__card--featured': testimonial.featured,
          }"
        >
          <div class="testimonials__rating" aria-label="5 estrelas">
            <Star
              v-for="star in testimonial.rating"
              :key="star"
              :size="18"
              fill="currentColor"
              aria-hidden="true"
            />
          </div>

          <p class="testimonials__text">“{{ testimonial.text }}”</p>

          <div class="testimonials__footer">
            <div>
              <strong>{{ testimonial.name }}</strong>

              <div class="testimonials__source">
                <BadgeCheck :size="16" aria-hidden="true" />

                <div class="testimonials__source-text">
                  <strong>Google Reviews</strong>
                  <span>★★★★★ 5 estrelas</span>
                </div>
              </div>
            </div>
          </div>
        </article>
      </div>
    </div>
  </section>
</template>
