<template>
  <div id="app">
    <div class="container">
      <VideoPlayer src="Dog on the beach.mp4" />
      <HelloWorld msg="Rick & Morty Characters" />
    </div>
    <AppBtn @click="remove">
      <template #secondrow="{ character }">
        {{ character.name }}
      </template>
    </AppBtn>
  </div>
</template>

<script setup>
import HelloWorld from "@/components/HelloWorld.vue";
import VideoPlayer from "./components/VideoPlayer.vue";
import AppBtn from "./components/AppBtn.vue";

</script>
