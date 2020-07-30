<template>
  <footer class="site-footer">
    {{ $siteConfig.siteName }} &copy; {{ new Date().getFullYear() }} - All
    Rights Reserved
    <br />
    Made with <span style="color: #e25555;">&#x263C;</span> with Nuxt.js and
    Netlify
  </footer>
</template>

<script>
export default {
  name: 'SiteFooter',
  mounted() {
    let hubspotscript = document.createElement('script')
    hubspotscript.setAttribute('src', '//js.hs-scripts.com/8194032.js')
    hubspotscript.setAttribute('id', 'hs-script-loader')
    hubspotscript.setAttribute('defer', '')
  },
}
</script>

<style scoped>
footer {
  background: #eee;
  padding: 20px 10px;
  text-align: center;
  transition: 0.5s ease all;
}
</style>
