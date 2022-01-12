<template>
  <div>
    <!-- -----------------------------------------------
    Banner
    ----------------------------------------------- -->
    <Banner />
    <!-- -----------------------------------------------
    ./ Banner
    ----------------------------------------------- -->
    <!-- -----------------------------------------------
    All Components
    ----------------------------------------------- -->
    <!-- <AllCustomComponents /> -->
    <!-- -----------------------------------------------
    ./ All Components
    ----------------------------------------------- -->
    <!-- -----------------------------------------------
    Coming Soon
    ----------------------------------------------- -->
    <ComingSoon />
    <!-- -----------------------------------------------
    ./ Coming Soon
    ----------------------------------------------- -->
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: "Elite Football",
      meta: [
       {
        hid: 'description',
        name: 'description',
        content: 'Join together with up to 7 friends, take on the elite in 5v5 intense competitive experience.',
      },
      ],
    };
  },

  data() {
    return {};
  },
  components: {
    Banner: () => import("@/components/shared/lp-banner/Banner"),
    ComingSoon: () => import("@/components/shared/coming-soon/ComingSoon"),
    AllCustomComponents: () =>
      import("@/components/custom/AllCustomComponents"),
  },
};
</script>
