<template>
  <v-item-group mandatory class="mt-n1">
    <v-container>
      <v-row justify="center" class="space">
        <v-col
          cols="12"
          xs="12"
          sm="4"
          md="2"
          v-for="(cetegory, i) in categories"
          :key="i"
        >
          <v-item v-slot="{ active, toggle }">
            <v-card
              :color="active ? '#0F136C' : 'white'"
              :class="active ? 'borderme' : 'borderout'"
              class="d-flex align-center rounded-lg mx-2"
              dark
              height="180"
              @click="toggle"
              flat
            >
              <v-row>
                <v-col cols="12" sm="12">
                  <v-list-item three-line class="text-center">
                    <v-list-item-content>
                      <div align="center" justify="center">
                        <v-img
                          :src="cetegory.img"
                          max-height="80"
                          max-width="80"
                          contain
                        ></v-img>
                      </div>
                      <v-list-item-subtitle
                        :class="active ? 'white--text' : 'black--text'"
                        class="caption mt-4"
                        >{{ cetegory.title }}</v-list-item-subtitle
                      >
                    </v-list-item-content>
                  </v-list-item>
                </v-col>
              </v-row>
            </v-card>
          </v-item>
        </v-col>
      </v-row>
    </v-container>
  </v-item-group>
</template>

<script>
export default {
  data: () => ({
    categories: [
      { img: "01.jpg", title: "Mobiles" },
      { img: "02.jpg", title: "Serum & Essence" },
      { img: "03.jpg", title: "Tablets" },
      { img: "04.jpg", title: "Air Purifiers" },
      { img: "05.jpg", title: "In-Ear Headphones" },
      { img: "06.jpg", title: "Plant, Seeds and Bulbs" },
    ],
  }),
};
</script>

<style>
</style>