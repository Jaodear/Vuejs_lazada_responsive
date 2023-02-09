<template>
  <v-app-bar app color="white" flat>
      <v-img src="1.png" contain width="100"></v-img>
    <v-card-text>
                <v-row>
                  <v-col cols="5">
                    <v-text-field
                      v-model="search"
                      append-icon="mdi-magnify"
                      label="Search"
                      single-line
                      hide-details
                    ></v-text-field>
                  </v-col>
                </v-row>
              </v-card-text>
        <v-icon x-middle color="#0F136C">fas fa-shopping-cart</v-icon>
      <v-img src="newuser.jpg" contain width="200"></v-img>
    <v-app-bar-nav-icon id="menu"
    color="#0F136C"
      ></v-app-bar-nav-icon>
    <div class="d-flex justify-space-around">
    <v-menu activator="#menu">
      <v-list>
        <v-list-item
          v-for="(item, index) in items"
          :key="index"
          :value="index"
        >
          <v-list-item-title>{{ item.title }}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu>
  </div>
  </v-app-bar>
  
</template>

<script>
export default {
    data: () => ({
      items: [
        { title: 'Save more on app' },
        { title: 'Sell on lazada' },
        { title: 'Custome Care' },
        { title: 'Track my order' },
        { title: 'Login' },
        { title: 'Sign up' },
      ],
    }),
  }
</script>

<style>
.v-toolbar__title {
  font-size: 1rem !important;
}
</style>