<script setup>
const props = defineProps(["model"]);
const rental = props.model;
</script>

<template>
  <article class="rental">
    <RentalImage :src="rental.image" :alt="`A picture of ${rental.title}`" />
    <div class="details">
      <h3>
        <NuxtLink :to="`/rental/${rental.id}`">
          {{ rental.title }}
        </NuxtLink>
      </h3>
      <div class="detail owner">
        <span>Owner: </span>
        {{ rental.owner }}
      </div>
      <div class="detail type">
        <span>Type: </span>
        {{ rental.type }}
      </div>
      <div class="detail location">
        <span>Location: </span>
        {{ rental.city }}
      </div>
      <div class="detail bedrooms">
        <span>Number of bedrooms: </span>
        {{ rental.bedrooms }}
      </div>
    </div>
  </article>
</template>
