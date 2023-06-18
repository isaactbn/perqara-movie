<template>
  <div class="view-wrapper">
    <navigation />
    <div style="min-height:75vh">
      <nuxt/>
    </div>
    <app-footer />
  </div>
</template>
<script>
import Navigation from '~/components/Navigation.vue'
import AppFooter from '~/components/AppFooter.vue'

export default {
  head: {
    link: [
      { rel: 'stylesheet', href: 'https://fonts.googleapis.com/css?family=Fjalla+One' }
    ]
  },
  components: {
    Navigation,
    AppFooter,
  }
}
</script>
<style>
.view-wrapper {
  background-color: #1E232B;
}
</style>
