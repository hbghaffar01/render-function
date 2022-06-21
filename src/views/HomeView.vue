<template>
  <HeadingView>TV Finder</HeadingView>
  <myShows>
    <template #sc="{ shows }">
      <h3 v-if="shows?.length > 0">
        Average Score {{ computedAverage(shows).toFixed(2) }}
      </h3>
    </template>
  </myShows>
</template>>

<script setup>
  import HeadingView from '@/components/HeadingView.vue'
  import myShows from '@/components/myShows.vue';

  const computedAverage = (shows) =>
  shows.reduce((acc, info) => +info.score + acc, 0) / shows.length;
</script>

<style>

</style>
