<template>
  <div>
    <h1 class="p-8 text-4xl text-center">
      {{ msg }}
    </h1>

    <CharacterCards />
  </div>
</template>

<script setup>
import CharacterCards from "@/components/CharacterCards.vue";

const props = defineProps(['msg'])

const ids = ([99])

</script>
