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
                Upcoming Fixtures
              </h2>
              <p class="white--text">Get your squad ready, here we go!</p>
            </div>
          </v-col>
        </v-row>

        <!-- -----------------------------------------------
            End Ui Table
        ----------------------------------------------- -->
      </v-container>
    </div>
    <div style="background-color: #212226">
      <v-container>
        <v-row justify="center">
          <v-col cols="12" sm="10" md="9" lg="7">
            <div class="text-center">
              <div class="pb-6">
                <v-btn v-on:click="$fetch" class="refresh-button" elevation="1"
                  >Refresh</v-btn
                >
                <!-- <select
                  class="form-control"
                  @change="changeLeague($event)"
                  v-on:click="$fetch"
                >
                  <option value="" selected disabled>Choose League</option>
                  <option
                    v-for="league in leagues"
                    :value="league.id"
                    :key="league.id"
                    class="refresh-button m-2"
                  >
                    {{ league.name }}
                  </option>
                </select> -->
              </div>

              <p v-if="$fetchState.pending" justify="center">
                Fetching fixtures...
              </p>
              <p v-else-if="$fetchState.error" justify="center">
                An error occurred :(
              </p>

              <v-card v-else>
                <v-card-text>
                  <v-simple-table>
                    <template v-slot:default>
                      <thead>
                        <tr>
                          <th>ID</th>
                          <th>Time</th>
                          <th>Home Team</th>
                          <th>Away Team</th>
                        </tr>
                      </thead>
                      <tbody>
                        <tr v-for="fixture in fixtures" :key="fixture.id">
                          <td style="text-align: center" rowspan="1">
                            {{ fixture.id }}
                          </td>
                          <!-- <td rowspan="1">{{ fixture.match_date }}</td> -->
                          <td style="text-align: center" rowspan="1">
                            {{ fixture.match_time }}
                          </td>
                          <td style="text-align: center" rowspan="1">
                            {{ fixture.teams[0].team.name }}
                          </td>
                          <td style="text-align: center" rowspan="1">
                            {{ fixture.teams[1].team.name }}
                          </td>
                        </tr>
                      </tbody>
                    </template>
                  </v-simple-table>
                </v-card-text>
              </v-card>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </div>
  </div>
</template>
<script>
export default {
  name: "UiFixtures",

  data() {
    return {
      fixtures: [],
    };
  },

  async fetch() {
    this.fixtures = await fetch(process.env.baseUrl + "/api/match/fixtures")
      .then((res) => res.json())
      .catch((err) => {
        console.error(err);
        this.$fetchState.error = true;
      });

    console.log(this.fixtures);
  },

  methods: {},
};
</script>
