<!-- Section divider: full gradient with heading and optional one-line description. -->
<template>
  <div class="slidev-layout">
    <div class="section-slide">
      <div class="section-gradient" />
      <Logo :src="$slidev.configs.logo" class="cover-logo" />
      <div class="section-content">
        <slot />
      </div>
    </div>
  </div>
</template>
