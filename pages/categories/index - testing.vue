<template>
  <div id="categories-page" class="page-wrapper categories-page">
    <site-hero
      title="Elements of Climate Cybernetics"
      subtitle="The basis vectors for engineering a climate economy"
      image="https://picsum.photos/1800/1801"
    />
    <main-section theme="one-column">
      <template v-slot:default>
        <div class="post-wrapper">
          <markdown :markdown="$store.state.content" />
        </div>
      </template>
    </main-section>
  </div>
</template>
<script>
import { mapState } from 'vuex'
// import 'highlight.js/styles/github.css'
import { setPageData } from '../../helper'
import Markdown from '~/components/Markdown'
export default {
  head() {
    return {
      title: `Categories | ${this.$siteConfig.siteName}`
    }
  },
  components: {
    Markdown
  },
  computed: {
    ...mapState([
      'title',
      'subtitle',
      'featureImage',
      'underSubtitle',
      'author',
      'category',
      'slug'
    ])
  },
  fetch({ store, params }) {
    setPageData(store, { resource: 'post', slug: params.singlePost })
  }
}
</script>
