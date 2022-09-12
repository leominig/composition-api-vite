<template>
  <div class="text-center">
    <video :src="src" ref="video" type="video/mp4" />
    <div v-if="video">
      <div class="btn-group">
        <button @click="video.play" class="btn btn-outline-primary me-4 mt-2">
          Play
        </button>
        <button @click="video.pause" class="btn btn-outline-primary mt-2">
          Pause
        </button>
      </div>
    </div>
  </div>
</template>

<script setup>
import { useGlobalEvent } from '@/composables/useGlobalEvent';
import { ref } from 'vue'

defineProps({
  src: String
})

useGlobalEvent("keypress",(e) => {
  if(e.chardCode!==32) return;

  video.value.paused? video.value.play():video.value.paused()
})

const video=ref(null)



</script>

<style lang="scss" scoped>
</style>