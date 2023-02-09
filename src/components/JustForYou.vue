<template>
  <v-row justify="center" class="space px-16 pb-5">
    <v-col cols="12" xs="12" sm="6" md="4" v-for="(JustForYou, i) in JustForYours" :key="i">
      <v-card class="mx-auto rounded-xl" max-width="300" color="" flat outlined>
        <div align="center" justify="center">
          <v-img
            max-height="300"
            max-width="300"
            contain
            :src="JustForYou.img"
          ></v-img>
        </div>

        <v-card-title class="">{{ JustForYou.title }}</v-card-title>
        <v-card-title class="orange--text mt-n4">{{ JustForYou.price }}</v-card-title>
        <v-card-title class="grey--text text-grey-darken-1 caption mt-n6">
          <div class="text-decoration-line-through">
          {{
            JustForYou.subtitle
          }}
          </div>
          <div class="font-weight-black">
          {{ 
            JustForYou.subtitle2 
          }}
          </div>
          </v-card-title>

          <v-card-title>
            <v-rating
              v-model="rating"
              color="yellow darken-3"
              background-color="grey darken-1"
              empty-icon="$ratingFull"
              half-increments
              hover
              small
            >
          </v-rating>
          <div class="grey--text text-grey-darken-1 caption">
              {{ 
                JustForYou.sum
              }}
            </div>
          </v-card-title>
      </v-card>
    </v-col>
    <v-btn> LOAD MORE </v-btn>
  </v-row>
</template>

<script>
export default {
  data: () => ({
    JustForYours: [
      { img: "p1.jpg", title: "บราวนี่โกโก้ บราวนี่จิ๋ว 1 ชิ้น", subtitle: "฿7.00", subtitle2: "-29%", price: "฿5.00", sum: "(351)"},
      { img: "p2.jpg", title: "กล่องผ้าพับได้ กล่องใส่เสื้อผ้าพับได้ กล่องอเนกประสงค์..", subtitle: "฿100.00", subtitle2: "-77%",  price: "฿23.00", sum: "(388)" },
      { img: "p3.jpg", title: "ส่งเร็ว🚚 รองเท้าแตะ ผู้หญิง ยางนิ่มแบบสวมรัดส้น รองเท้า..", subtitle: "฿259.00", subtitle2: "-75%", price: "฿64.00", sum: "(2755)" },
      { img: "p4.jpg", title: "CAY🌟ราวตากผ้า แขวนเสื้อผ้า Coat Rack ราวแขวนเสื้อ..", subtitle: "฿376.00", subtitle2: "-76%", price: "฿89.00", sum: "(2019)" },
      { img: "p5.jpg", title: "โคมไฟตั้งโต๊ะ โคมไฟอ่านหนังสือ LED โคมไฟหัวเตียง..", subtitle: "฿115.82.00", subtitle2: "-40%", price: "฿69.00", sum: "(891)" },
      { img: "p6.jpg", title: "ผ้าม่าน ม่าน ม่าน ม่านเวลโคร ม่านทึบแสง ม่านกันฝุ่น ติดตั้ง..", subtitle: "฿169.00", subtitle2: "-70%", price: "฿50.00", sum: "(1423)" },
    ],
    rating: 5
  })
}
</script>

<style>
</style>