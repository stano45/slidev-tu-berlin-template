<!-- Title slide: white top with the long logo, blue-green gradient below. -->
<template>
  <div class="slidev-layout">
    <div class="cover-bg" />
    <div class="cover-gradient-shape" />
    <Logo :src="$slidev.configs.logoLong" class="cover-logo" />
    <div class="cover-content">
      <slot />
      <p v-if="$slidev.configs.footer" class="author">{{ $slidev.configs.footer }}</p>
    </div>
  </div>
</template>
