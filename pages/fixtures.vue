<template>
  <div>
    <ui-fixtures />
    <ComingSoon />
  </div>
</template>

<script>
import UiFixtures from "../components/basic/UiFixtures.vue";
export default {
  head() {
    return {
      title: "Fixtures",
      meta: [
        {
          hid: "description",
          name: "Elite Football - Fixtures",
          content: "Find Out when you ball",
        },
      ],
    };
  },

  data() {
    return {};
  },
  components: {
    BannerTwo: () => import("@/components/shared/lp-banner/BannerTwo"),

    ComingSoon: () => import("@/components/shared/coming-soon/ComingSoon"),
    UiFixtures: () => import("@/components/basic/UiFixtures.vue"),

    // UiForm: () => import("../components/basic/UiForm"),
    // AllComponents: () => import("@/components/basic/AllComponents"),
  },
};
</script>
