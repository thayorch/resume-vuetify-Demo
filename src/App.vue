<template>
  <v-app>
    <v-main>
      <button @click="toggleLanguage" class="ma-3 lang ">
        {{ currentLang }}
      </button>

      <v-container>
        <v-sheet class="text-body-2 mx-auto">
          <div class="d-flex flex-wrap">
            <v-row class="row">
              <v-col md="2" class="resume-img-contianer">
                <v-img
                  src="/src/assets/resume-image.jpg"
                  width="200"
                  class="resume-img"
                ></v-img>
              </v-col>

              <v-col md="5" class="mt-2">
                <h1 class="py-1">{{ translate.names }}</h1>
                <h2 class="py-1">
                  <v-icon>mdi-access-point</v-icon> {{ translate.title }}
                  <v-icon>mdi-access-point</v-icon>
                </h2>
                <ul>
                  <li class="py-1">
                    <a :href="'mailto:' + translate.email[0]">{{
                      translate.email[0]
                    }}</a>
                  </li>
                  <li class="py-1">
                    <a :href="'mailto:' + translate.email[1]">{{
                      translate.email[1]
                    }}</a>
                  </li>
                  <li class="py-1">{{ translate.state }}</li>
                </ul>

                <div class="pt-4">
                  <h1>
                    <a href="https://www.facebook.com/lnwice0" target="_blank"
                      ><v-icon class="text-black">mdi-facebook</v-icon></a
                    >
                    <a
                      href="https://www.instagram.com/_i.icez5__/"
                      target="_blank"
                      ><v-icon class="text-black">mdi-instagram</v-icon></a
                    >
                    <a href="https://www.reddit.com/user/Thayorch101/" target="_blank"
                      ><v-icon class="text-black">mdi-reddit</v-icon></a
                    >
                    <a href="https://github.com/thayorch" target="_blank"
                      ><v-icon class="text-black">mdi-github</v-icon></a
                    >
                  </h1>
                </div>
              </v-col>
              <v-divider></v-divider>

              <v-row class="ma-2">
                <h1 class="pl-2 pt-2">Content</h1>
                <v-col md="auto" cols="12">
                  {{ translate.content }}
                </v-col>
              </v-row>
              <v-divider></v-divider>
              <v-row class="ma-2">
                <h1 class="pl-2 pt-2">Content</h1>
                <v-col md="auto" cols="12">
                  {{ translate.content }}
                </v-col>
              </v-row>
              <v-divider></v-divider>
              <v-row class="ma-2">
                <h1 class="pl-2 pt-2">Content</h1>
                <v-col md="auto" cols="12">
                  {{ translate.content }}
                </v-col>
              </v-row>
              <v-divider></v-divider>
              <v-row class="ma-2">
                <h1 class="pl-2 pt-2">Content</h1>
                <v-col md="auto" cols="12">
                  {{ translate.content }}
                </v-col>
              </v-row>
              <v-divider></v-divider>


            </v-row>
          </div>
        </v-sheet>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import { ref } from "vue";
export default {
  data() {
    return {
      translations: {
        EN: ref({
          email: [
            "thatcharnon.maidee@gmail.com",
            "thatcharnon.10210@gmail.com",
          ],
          state: "Chaing Mai, Thailand",
          names: "Thatcharnon Maidee",
          title: "Frontend Developer",
          nickname: "ICE",
          content:
            " Lorem ipsum dolor sit amet consectetur adipisicing elit. Eligendi nemo quasi ipsam, dolorum ipsa inventore velit veritatis quod a laudantium. Libero corrupti quo numquam molestiae provident quos eaque commodi blanditiis assumenda ex debitis consequatur perspiciatis voluptatem enim cupiditate quaerat, adipisci laboriosam fugiat inventore aliquid ipsam? Temporibus optio ut suscipit nisi, adipisci nihil quo cum exercitationem similique modi nulla maiores, velit, autem quasi corporis incidunt est doloremque vitae officia ea. Voluptas praesentium sunt itaque aperiam accusantium ipsa minus, debitis eligendi corrupti vitae odio. Ad, et ipsam dignissimos error est dolore eveniet. Quaerat dolor provident recusandae explicabo hic totam voluptatum unde molestiae!",
        }),

        TH: ref({
          email: [
            "thatcharnon.maidee@gmail.com",
            "thatcharnon.10210@gmail.com",
          ],
          state: "เชียงใหม่, ประเทศไทย",
          names: "ธัชนนท์ ใหม่ดี",
          title: "หน้าเว็บเดฟเวล็อปเปอร์",
          nickname: "ไอซ์",
          content:
            "รัมคอร์ปอเรชั่นชินบัญชร หน่อมแน้มแคร์สงบสุขมาเฟีย จิ๊กเคลียร์เดโมจิ๊กซอว์พาสต้า มือถืออวอร์ดแฮมเบอร์เกอร์วิดีโอคอนแท็ค แอ็กชั่นพฤหัสไบโอ ซานตาคลอสศากยบุตรสไตล์ดีพาร์ตเมนท์ คลาสสิก เพลย์บอยทีวีดิสเครดิตพฤหัส สหรัฐเมคอัพสปิริตคอนโดมิเนียม คำสาปวอล์กกษัตริยาธิราช ฮีโร่น็อกเทคโนแครต ปาสคาลเซลส์แมน แรลลีแดนซ์ชนะเลิศยูวีกาญจนาภิเษก พรีเซ็นเตอร์รีสอร์ต อริยสงฆ์แบรนด์ คาเฟ่คอร์รัปชันฮิแอพพริคอทสเตอริโอ",
        }),
      },
      currentLang: "EN",
    };
  },
  computed: {
    translate() {
      return this.translations[this.currentLang];
    },
  },
  methods: {
    toggleLanguage() {
      this.currentLang = this.currentLang === "EN" ? "TH" : "EN";
    },
  },
};
</script>
