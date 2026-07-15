<script setup>
import { ref } from "vue";
import { specialties } from "../../data/specialties";
import "./Specialties.css";
import SectionTitle from "../common/SectionTitle/SectionTitle.vue";

const activeSpecialtyId = ref(null);

function toggleSpecialty(id) {
  activeSpecialtyId.value = activeSpecialtyId.value === id ? null : id;
}
</script>

<template>
  <section class="specialties" id="especialidades">
    <div class="specialties__container">
      <SectionTitle
        eyebrow="Especialidades"
        title="Um cuidado pensado para diferentes necessidades"
        description="Conheça as abordagens utilizadas no Studio Vitta Pilates e descubra qual delas mais combina com seus objetivos."
      />

      <div class="specialties__list">
        <article
          v-for="specialty in specialties"
          :key="specialty.id"
          class="specialties__card"
          :class="{
            'specialties__card--active': activeSpecialtyId === specialty.id,
          }"
        >
          <button
            class="specialties__button"
            type="button"
            :aria-expanded="activeSpecialtyId === specialty.id"
            @click="toggleSpecialty(specialty.id)"
          >
            <span>{{ specialty.title }}</span>

            <span
              class="specialties__icon"
              :class="{
                'specialties__icon--active': activeSpecialtyId === specialty.id,
              }"
              aria-hidden="true"
            >
              <svg
                viewBox="0 0 24 24"
                width="18"
                height="18"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M6 9L12 15L18 9"
                  stroke="currentColor"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
              </svg>
            </span>
          </button>

          <Transition name="specialty-content">
            <div
              v-if="activeSpecialtyId === specialty.id"
              class="specialties__content"
            >
              <p>{{ specialty.description }}</p>
            </div>
          </Transition>
        </article>
      </div>
    </div>
  </section>
</template>
