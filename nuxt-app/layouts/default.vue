<template>
  <v-app dark>
    <Navigator />
    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>
    <Footer />
  </v-app>
</template>

<script>
import Navigator from '@/components/Navigator'
import Footer from '@/components/Footer'
export default {
  components: {
    Navigator,
    Footer,
  },
}
</script>
