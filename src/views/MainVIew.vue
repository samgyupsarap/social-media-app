<script setup lang="ts">
import ProfileSide from '@/components/ProfileSide.vue'
import MainContent from '@/components/MainContent.vue'
import AdContent from '@/components/AdContent.vue'
</script>

<template>
  <div class="grid grid-cols-12 gap-4 container mx-auto px-4 py-6">
    <div class="col-span-3">
      <ProfileSide />
    </div>
    <div class="col-span-6">
      <MainContent />
    </div>
    <div class="col-span-3">
      <AdContent />
    </div>
  </div>
</template>
