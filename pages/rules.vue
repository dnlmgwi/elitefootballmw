<template>
  <div>
    <div class="mini-spacer" style="background-color: #212226">
      <v-container>
        <!-- -----------------------------------------------
            Start Ui Table
        ----------------------------------------------- -->
        <v-row justify="center">
          <v-col cols="12" sm="10" md="9" lg="7">
            <div class="text-center">
              <h2 class="banner-title font-weight-bold white--text">
                {{ page.title }}
              </h2>
              <p class="white--text">We play by the rules.</p>
            </div>
          </v-col>
        </v-row>

        <!-- -----------------------------------------------
            End Ui Table
        ----------------------------------------------- -->
      </v-container>
    </div>
    <v-container>
      <!-- -----------------------------------------------
            Start Banner
        ----------------------------------------------- -->
      <div class="p-5 text-neutral-500">
        <article>
          <h1></h1>
          <nuxt-content :document="page" class="text-neutral-500" />
        </article>
      </div>

      <!-- -----------------------------------------------
            End Banner
        ----------------------------------------------- -->
    </v-container>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: "Rules",
      meta: [
        {
          hid: "description",
          name: "Elite Football - Rules",
          content: "Find Out the Rules of Elite Football",
        },
      ],
    };
  },
  async asyncData({ $content }) {
    const page = await $content("rules").fetch();

    return {
      page,
    };
  },

  components: {
    BannerRules: () => import("@/components/shared/lp-banner/BannerRules"),
    ComingSoon: () => import("@/components/shared/coming-soon/ComingSoon"),

    // UiForm: () => import("../components/basic/UiForm"),
    // AllComponents: () => import("@/components/basic/AllComponents"),
  },
};
</script>
