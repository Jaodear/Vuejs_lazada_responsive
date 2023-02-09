<template>
  <v-row justify="center" class="space px-16">
    <v-col
      cols="12"
      xs="12"
      sm="6"
      md="4"
      v-for="(FlashSale, i) in FlashSale"
      :key="i"
    >  
    <v-card class="mx-auto rounded-xl" max-width="300" color="" flat outlined>
        <div align="center" justify="center">
          <v-img
            max-height="300"
            max-width="300"
            contain
            :src="FlashSale.img"
          ></v-img>
        </div>

     <v-card-title class="">{{ FlashSale.title }}</v-card-title>
     <v-card-title class="orange--text mt-n4">{{ FlashSale.price }}</v-card-title> 
        <v-card-title class="grey--text text-grey-darken-1 caption mt-n6">
          <div class="text-decoration-line-through">
          {{
            FlashSale.subtitle
          }}
          </div>
          <div class="font-weight-black">
          {{ 
            FlashSale.subtitle2 
          }}
          </div>
        </v-card-title>

      </v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data: () => ({
    FlashSale: [
      { img: "pr1.jpg", title: "ถุงyeti ถุงใส่แก้วเยติ กระเป๋าใส่แก้วเยติ ถุงใส่แก้วเก็บความ..", subtitle: "฿30.00", subtitle2: "-63%", price: "฿11.00" },
      { img: "pr2.jpg", title: "เบ็ดตกปลาครบชุด รอกหยดน้ำพร้อมคัน รอกเบสพร้อม..", subtitle: "฿1,165.00", subtitle2: "-83%", price: "฿193.60" },
      { img: "pr3.jpg", title: "มีสิทธิรับ❗❗ [วันที่ 9 ก.พ. 66] Samsung Galaxy A13...", subtitle: "฿6,499.00", subtitle2: "-99%", price: "฿1.00" },
      { img: "pr4.jpg", title: "หูฟังบลูทูธ 5.0 ชุดหูฟัง Y30 TWS หูฟังไร้สาย ลดเสียง..", subtitle: "฿152.00", subtitle2: "-81%", price: "฿36.00" },
      { img: "pr5.jpg", title: "ของเล่น รูบิค ลูกบิด รูบิค 3x3 ของเล่นเด็ก ความเร็วระดับมือ..", subtitle: "฿39.00", subtitle2: "-77%", price: "฿9.00" },
      { img: "pr6.jpg", title: "เคส iPad รูปตัว Y Air1/Air2/Gen5/Gen6 9.7..", subtitle: "฿119.00", subtitle2: "-60%", price: "฿48.00" },
    ],
  })
};
</script>

<style>
</style>