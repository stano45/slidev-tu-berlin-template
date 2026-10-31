<!--
  Title + two columns. Default slot is the title, then ::left:: and ::right::.
  Frontmatter `cols` sets the column ratio (default '1fr 1fr'), e.g. cols: 3fr 2fr
-->
<template>
  <ContentFrame>
    <slot />
    <div class="slide-body split" :style="{ gridTemplateColumns: $frontmatter.cols || '1fr 1fr' }">
      <div class="split-text">
        <slot name="left" />
      </div>
      <div class="split-visual">
        <slot name="right" />
      </div>
    </div>
  </ContentFrame>
</template>
