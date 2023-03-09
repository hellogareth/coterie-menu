<template>
  <div>
    <!-- <vue-pdf-embed source="brunch.pdf" /> -->
    <vue-pdf-embed source="lunch.pdf" />
    <!-- <vue-pdf-embed source="dinner.pdf" /> -->
    <vue-pdf-embed source="drinks.pdf" />
    <!-- <vue-pdf-embed source="happy-hour.pdf" /> -->
    <vue-pdf-embed source="elevenses-drinks.pdf" />
  </div>
</template>

<script>

import VuePdfEmbed from 'vue-pdf-embed'

export default {
  name: 'PDFViewer',
  components: {
    VuePdfEmbed,
  },
  data() {
    return {
      source1: '<PDF_URL>',
        source2: '<PDF_URL>',
          source3: '<PDF_URL>',
            source4: '<PDF_URL>',
              source5: '<PDF_URL>',

                source6: '<PDF_URL>',
    }
  },
}
</script>