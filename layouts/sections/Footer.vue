<template>
  <!-- -----------------------------------------------
        Start Footer
  ----------------------------------------------- -->
  <v-footer class="footer">
    <v-container>
      <v-row class="py-0 py-md-15">
        <!-- -----------------------------------------------
        First Column
      ----------------------------------------------- -->
        <!-- <v-col cols="12" sm="12" md="12" lg="3" class="px-xs-0">
          <h4 class="font-weight-regular font-18">Address</h4>
          <p class="mt-10">71 Amsteroum Avenue Cronish Night, NY 35098</p>
        </v-col> -->
        <!-- -----------------------------------------------
        Second Column
      ----------------------------------------------- -->
        <v-col cols="12" sm="12" md="12" lg="3" class="px-xs-0">
          <h4 class="font-weight-regular font-18">Phone</h4>
          <p class="mt-10 mb-0">
            Frank:
            <a class="mt-10 mb-0" href="https://wa.me/265885374883"
              >+265 885 37 48 83</a
            >
          </p>
          <p class="mt-10 mb-0">
            Michael:
            <a class="mt-10 mb-0" href="https://wa.me/265994461051"
              >+265 994 46 10 51</a
            >
          </p>
          <p class="mt-10 mb-0">
            Daniel:
            <a class="mt-10 mb-0" href="https://wa.me/265997176756"
              >+265 997 17 67 56</a
            >
          </p>
        </v-col>
        <!-- -----------------------------------------------
        Third Column
      ----------------------------------------------- -->
        <v-col cols="12" sm="12" md="12" lg="3" class="px-xs-0">
          <h4 class="font-weight-regular font-18">Email</h4>
          <p class="mt-10 mb-0">
            Office :
            <a class="dark-link" href="mailto:elitefootballmalawi@gmail.com"
              >elitefootballmalawi@gmail.com</a
            >
          </p>
          <p>
            Site :
            <a class="dark-link" href="https://elitefootballmw.vercel.app/"
              >elitefootballmw.vercel.app</a
            >
          </p>
        </v-col>
        <!-- -----------------------------------------------
        Fourth Column
      ----------------------------------------------- -->
        <v-col cols="12" sm="12" md="12" lg="3" class="px-xs-0">
          <h4 class="font-weight-regular font-18">Social</h4>

          <div class="social-icons mt-10">
            <!-- <a href="https://web.facebook.com/EliteFootballmw">
              <i class="mdi mdi-facebook"></i>
            </a> -->
            <a href="https://twitter.com/EliteFootballmw" target="_blank">
              <i class="mdi mdi-twitter"></i>
            </a>
            <!-- <a href="#">
              <i class="mdi mdi-google-plus"></i>
            </a> -->
            <!-- <a href="#">
              <i class="mdi mdi-youtube"></i>
            </a> -->
            <!-- <a href="https://www.instagram.com/elitefootballmw">
              <i class="mdi mdi-instagram"></i>
            </a> -->
          </div>
        </v-col>
      </v-row>
      <div class="footer-bottom-bar font-14">
        <div class="d-block d-md-flex align-center">
          <p>
            All Rights Reserved by
            <a href="https://elitefootballmw.vercel.app/" class="link"
              >Elite Sports Group Malawi</a
            >
          </p>
          <div class="ml-auto">
            <div class="d-flex align-center">
              <a href="/" class="link px-4">Terms of Use</a>
              <a href="/" class="link px-4">Legal Disclaimer</a>
              <a href="/" class="link px-4">Privacy Policy</a>
            </div>
          </div>
        </div>
      </div>
    </v-container>
  </v-footer>
  <!-- -----------------------------------------------
        End Footer
  ----------------------------------------------- -->
</template>

<script>
export default {
  name: "Footer",
  data() {
    return {
      data: [],
    };
  },
  components: {},
};
</script>
