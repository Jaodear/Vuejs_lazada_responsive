<template>
  <v-app>
    <Navbar />
    <v-container fluid>
      <v-row>
        <v-col cols="12">
          <v-carousel :show-arrows="false">
            <v-carousel-item
              v-for="(item,i) in items"
              :key="i"
              :src="item.src"
              cover
              max-height="100%" max-width="100%" contain
            ></v-carousel-item>
          </v-carousel>

          <v-toolbar flat color="transparent" class="mt-5">
            <v-toolbar-title class="text-h6">Flash Sale</v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn rounded color="#0F136C" dark class="px-8">SHOP ALL PRODUCTS</v-btn>
          </v-toolbar>
          <FlashSale />

          <v-toolbar flat color="transparent">
            <v-toolbar-title class="text-h6">Categories</v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn-toggle v-model="toggle_exclusive" group color="#0F136C">
              <v-btn>
                <v-icon>mdi-chevron-left</v-icon>
              </v-btn>
              <v-btn>
                <v-icon>mdi-chevron-right</v-icon>
              </v-btn>
            </v-btn-toggle>
          </v-toolbar>
          <Category />

          <v-card flat color="transparent" class="mt-8">
            <v-toolbar flat color="transparent" class="mb-4">
              <v-toolbar-title class="text-h6 mt-5"
                >Just For You</v-toolbar-title
              >
            </v-toolbar>
            <JustForYou />

          </v-card>
        </v-col>
      </v-row>
    </v-container>

    <Footer />
  </v-app>
</template>

<script>
import Navbar from "../components/Navbar";
import Footer from "../components/Footer";
import Category from "../components/Category.vue";
import FlashSale from "../components/FlashSale.vue";
import JustForYou from "../components/JustForYou.vue";
export default {
  name: "Home",
  data: () => ({
    toggle_exclusive: 1
  ,
        items: [
          {
            src: "cover1.jpg",
          },
          {
            src: "cover2.jpg",
          },
          {
            src: "cover3.jpg",
          },
          {
            src: "cover4.jpg",
          },
          {
            src: "cover5.jpg",
          },
          {
            src: "cover6.jpg",
          },
          {
            src: "cover7.jpg",
          },
          {
            src: "cover8.jpg",
          },
        ],
        slides: [
          'First',
          'Second',
          'Third',
          'Fourth',
          'Fifth',
        ],
      }),

  components: {
    Navbar,
    Footer,
    Category,
    FlashSale,
    JustForYou
  },
};
</script>
<style >
.marginLeft {
  margin-left: -90px;
}
.mtop {
  margin-top: 100px;
}
.mbottom {
  margin-bottom: 100px;
}
.v-card.borderme {
  border: 2px solid #0F136C !important;
}
.v-card.borderout {
  border: 1px solid #f0d5dc !important;
}
.v-btn:not(.v-btn--round).v-size--default.add {
  min-width: 0px !important;
}
.theme--light.v-sheet--outlined.mobile {
  border: 2px solid black !important;
}
@media only screen and (max-width: 600px) {
  h2.title1 {
    font-size: 15px;
  }
  h2.title2 {
    font-size: 15px;
  }
  .top {
    margin-top: 20px;
  }
}
@media only screen and (min-width: 600px) {
  .top {
    margin-top: 70px;
  }
}
@media only screen and (min-width: 768px) {
  .top {
    margin-top: 120px;
  }
}
</style>
