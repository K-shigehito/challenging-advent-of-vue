<script setup lang="ts">
import TopHeading from "@/components/UI/TopHeading.vue";
import PageDay2 from "@/components/day-2/PageDay2.vue";
</script>

<template>
  <main>
    <TopHeading>
      <template v-slot:day> Day 2 </template>
      joke generator
    </TopHeading>
    <div class="mt-10">
      <PageDay2 />
    </div>
  </main>
</template>
