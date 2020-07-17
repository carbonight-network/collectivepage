<template>
  <div id="categories-page" class="page-wrapper categories-page">
    <site-hero
      title="Elements of Climate Cybernetics"
      subtitle="The basis vectors for engineering a climate economy"
      image="/logo-cnn.png"
    />
    <main-section theme="one-column">
      <categories-grid />
    </main-section>
  </div>
</template>
<script>
export default {
  head() {
    return {
      title: `Categories | ${this.$siteConfig.siteName}`
    }
  }
}
</script>
