<template>
  <v-app dark>
    <!--v-if="$route.name!=='login'"-->
    <Header />
    <v-main>
      <nuxt />
    </v-main>
    <Footer />
  </v-app>
</template>

<script>
export default {
  head() {
    return {
      title: "Elite Football",
      meta: [
        {
          hid: "description",
          name: "description",
          content: "Join together with up to 7 friends, take on the elite in 5v5 intense competitive experience."
        }
      ]
    };
  },
  components: {
    Header: () => import("@/layouts/sections/Header"),
    Footer: () => import("@/layouts/sections/Footer")
  },
  methods: {}
};
</script>

<style></style>
