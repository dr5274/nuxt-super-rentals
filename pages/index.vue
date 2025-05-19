<script setup>
import { useRentals } from "@/composables/useRentals";
const { model } = useRentals();
</script>

<template>
  <Jumbo>
    <template #content>
      <h2>Welcome to Super Rentals!</h2>
      <p>We hope you find exactly what you're looking for in a place to stay.</p>
      <NuxtLink to="/about" class="button"> About Us </NuxtLink>
    </template>
  </Jumbo>
  <Rentals :model="model" />
</template>
