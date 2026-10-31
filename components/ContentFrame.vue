<!-- Shared chrome for content slides: logo top right, gradient footer with page number. -->
<template>
  <div class="slidev-layout">
    <Logo :src="$slidev.configs.logo" class="slide-logo" />
    <div class="content-slide">
      <slot />
    </div>
    <div v-if="!$frontmatter.hideFooter" class="slide-footer">
      <span class="page-no">Slide <SlideCurrentNo /></span>
      <span v-if="$slidev.configs.footer">{{ $slidev.configs.footer }}</span>
    </div>
  </div>
</template>
