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
                League Table
              </h2>
              <p class="white--text">
                Bring your squad & unique style of play, challenge the best &
                climb the ranks.
              </p>
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
              <!-- <select class="form-control" @change="changeLeague($event)">
                <option value="" selected disabled>Choose</option>
                <option
                  v-for="league of leagues"
                  :value="league.id"
                  :key="league.id" style="color: #000000"
                >
                  {{ league.data.id }}
                </option> -->
              <!-- </select> -->
              <!-- <v-btn v-on:click="$fetch" class="refresh-button" elevation="1"
                >Refresh</v-btn
              > -->
              <p v-if="$fetchState.pending" justify="center">
                Fetching teams...
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
                          <th></th>
                          <th>Name</th>
                          <th>GP</th>
                          <th>W</th>
                          <th>D</th>
                          <th>L</th>
                          <th>GD</th>
                          <th>Pts</th>
                        </tr>
                      </thead>
                      <tbody>
                        <tr v-for="team in teams" :key="team.id">
                          <td style="text-align: center" rowspan="1">
                            {{ team.rank }}
                          </td>
                          <td rowspan="1">{{ team.name }}</td>
                          <td style="text-align: center" rowspan="1">
                            {{ team.played }}
                          </td>
                          <td style="text-align: center" rowspan="1">
                            {{ team.won }}
                          </td>
                          <td style="text-align: center" rowspan="1">
                            {{ team.draw }}
                          </td>
                          <td style="text-align: center" rowspan="1">
                            {{ team.lost }}
                          </td>
                          <td style="text-align: center" rowspan="1">
                            {{ team.goalDifference }}
                          </td>
                          <td style="text-align: center" rowspan="1">
                            {{ team.points }}
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
  name: "UiTable",
  data() {
    console.log(this.leagues);
    return {
      teams: [],
      leagues: [],
      selectedLeague: null,
    };
  },

  async fetch() {
    this.teams = await fetch(
      "https://radiant-wildwood-51737.herokuapp.com/api/leagues/table/1"
    )
      .then((res) => res.json())
      .catch((err) => {
        console.error(err);
        this.$fetchState.error = true;
      });

    // this.leagues = await fetch(
    //   "https://radiant-wildwood-51737.herokuapp.com/api/leagues"
    // )
    //   .then((res) => res.json())
    //   .catch((err) => {
    //     console.error(err);
    //     this.$fetchState.error = true;
    //   });
  },
  methods: {
    changeLeague(event) {
      this.selectedLeague =
        event.target.options[event.target.options.selectedIndex].text;
    },
  },
};
</script>
