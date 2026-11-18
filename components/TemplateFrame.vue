<script setup lang="ts">
withDefaults(defineProps<{
  variant?: 'cover' | 'chapter' | 'content' | 'image'
}>(), { variant: 'content' })
</script>

<template>
  <div class="slidev-layout th-slide" :class="`th-${variant}`">
    <img
      class="th-logo"
      :src="variant === 'cover' ? '/branding/logo-white.png' : variant === 'chapter' ? '/branding/logo-white-small.png' : '/branding/logo-blue.png'"
      alt="Technische Hochschule Mannheim"
    />
    <img v-if="variant === 'cover'" class="th-cover-mark" src="/branding/cover-mark.svg" alt="" />
    <main class="th-content"><slot /></main>
    <footer class="th-footer">Technische Hochschule Mannheim | Professor | {{ $slidev.configs.author }}</footer>
    <span v-if="variant !== 'cover'" class="th-page">{{ $slidev.nav.currentPage }}</span>
  </div>
</template>
