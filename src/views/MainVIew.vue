<script setup lang="ts">
import ProfileSide from '@/components/ProfileSide.vue'
import MainContent from '@/components/MainContent.vue'
import AdContent from '@/components/AdContent.vue'
</script>

<template>
  <div class="max-w-8xl grid grid-cols-12 gap-4 mx-auto px-4 py-6">
    <div class="col-span-3">
      <ProfileSide />
    </div>
    <div class="col-span-7">
      <MainContent />
    </div>
    <div class="col-span-2">
      <AdContent />
    </div>
  </div>
</template>
