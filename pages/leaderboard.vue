<template>
  <div>
    <ui-table />
    <ComingSoon />
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: "Leaderboard",
      meta: [
        {
          hid: "description",
          name: "Elite Football - Leaderboard",
          content: "Find Out where you stand in the ranks",
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
    UiTable: () => import("@/components/basic/UiTable.vue"),
    
    // UiForm: () => import("../components/basic/UiForm"),
    // AllComponents: () => import("@/components/basic/AllComponents"),
  },
};
</script>
