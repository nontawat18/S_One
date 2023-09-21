<template>
  <div class="">
    <ScrollToTopButton v-if="mobile < 1100" />
        <v-col>
      <v-row>
        <v-col cols="12" md="12" lg="3">
          <div v-if="mobile < 1100">
            <v-text-field
              dark
              dense
              solo
              hide-details
              label="ค้นหายาง"
              append-icon="mdi-magnify"
              background-color="#f05a28"
            ></v-text-field>
          </div>
          <div v-else>
            <div class="head-search"><h3>ค้นหายาง</h3></div>
            <v-img
              :src="require('~/assets/images/SOne_index_bg_searchtype.jpg')"
            >
              <v-row>
                <v-col cols="4"> </v-col>
                <v-col cols="8" class="">
                  <v-col class="pl-0 pt-0">
                    <h4>หน้ายาง</h4>
                    <small>ความกว้าง (มม.)</small>
                    <v-select
                      dense
                      solo
                      hide-details
                      label="--เลือกหน้ายาง--"
                    ></v-select>
                  </v-col>
                  <v-col class="pl-0 pt-0">
                    <h4>ซีรี่ย์</h4>
                    <small>อัตราส่วนความสูงแก้มยาง (%)</small>
                    <v-select
                      dense
                      solo
                      hide-details
                      label="--เลือกซีรี่ย์--"
                    ></v-select>
                  </v-col>
                  <v-col class="pl-0 pt-0">
                    <h4>กระทะล้อ</h4>
                    <small>เส้นผ่าศูนย์กลาง (นิ้ว)</small>
                    <v-select
                      dense
                      solo
                      hide-details
                      label="--เลือกกระทะล้อ--"
                    ></v-select>
                  </v-col>
                </v-col>
              </v-row>
            </v-img>
          </div>
        </v-col>
        <v-col cols="12" md="12" lg="9" v-if="mobile > 1100" class="pl-0">
          <div>
            <v-img
              :src="require('~/assets/images/SOne_index_news_23.jpg')"
              height="340px"
            >
              <v-col>
                <v-row align="center" justify="center">
                  <v-col cols="10"></v-col>
                  <v-col cols="2">
                    <div class="pb-2 pl-12 pt-4">
                      <v-img
                        :src="require('~/assets/images/SOne_index_arrowup.png')"
                        width="40%"
                      >
                      </v-img>
                    </div>
                    <div style="border: solid 1px #f05a28">
                      <v-img
                        :src="require('~/assets/images/SOne_index_pic01.jpg')"
                      >
                      </v-img>
                    </div>

                    <div class="pb-2 pt-2">
                      <v-img
                        :src="require('~/assets/images/SOne_index_pic02.jpg')"
                      >
                      </v-img>
                    </div>
                    <div class="pb-2">
                      <v-img
                        :src="require('~/assets/images/SOne_index_pic02.jpg')"
                      >
                      </v-img>
                    </div>
                    <div class="pb-2 pl-12">
                      <v-img
                        :src="
                          require('~/assets/images/SOne_index_arrowdown.png')
                        "
                        width="40%"
                      >
                      </v-img>
                    </div>
                  </v-col>
                </v-row>
              </v-col>
            </v-img>
          </div>
        </v-col>
        <v-col cols="12" md="12" lg="9" v-else class="pa-0">
          <v-img :src="require('~/assets/images/SOne_index_news_23.jpg')">
          </v-img>
        </v-col>
      </v-row>
    </v-col>
    <v-col>
      <v-row class="pt-2">
        <v-col cols="12" lg="2" md="2" class="pt-0">
          <v-hover v-slot="{ hover }">
            <v-card :elevation="hover ? 0 : 0" :class="{ 'on-hover': hover }">
              <v-img :src="require('~/assets/images/SOne_index_bt-tire1.jpg')">
              </v-img>
            </v-card>
          </v-hover>
        </v-col>
        <v-col cols="12" lg="2" md="2" class="pt-0">
          <v-hover v-slot="{ hover }">
            <v-card :elevation="hover ? 0 : 0" :class="{ 'on-hover': hover }">
              <v-img :src="require('~/assets/images/SOne_index_bt-break1.jpg')">
              </v-img>
            </v-card>
          </v-hover> </v-col
        ><v-col cols="12" lg="2" md="2" class="pt-0">
          <v-hover v-slot="{ hover }">
            <v-card :elevation="hover ? 0 : 0" :class="{ 'on-hover': hover }">
              <v-img
                :src="require('~/assets/images/SOne_index_bt-battery1.jpg')"
              >
              </v-img>
            </v-card>
          </v-hover> </v-col
        ><v-col cols="12" lg="2" md="2" class="pt-0">
          <v-hover v-slot="{ hover }">
            <v-card :elevation="hover ? 0 : 0" :class="{ 'on-hover': hover }">
              <v-img
                :src="require('~/assets/images/SOne_index_bt-chokeup1.jpg')"
              >
              </v-img>
            </v-card>
          </v-hover> </v-col
        ><v-col cols="12" lg="2" md="2" class="pt-0">
          <v-hover v-slot="{ hover }">
            <v-card :elevation="hover ? 0 : 0" :class="{ 'on-hover': hover }">
              <v-img :src="require('~/assets/images/SOne_index_bt-oil1.jpg')">
              </v-img>
            </v-card>
          </v-hover> </v-col
        ><v-col cols="12" lg="2" md="2" class="pt-0">
          <v-hover v-slot="{ hover }">
            <v-card :elevation="hover ? 0 : 0" :class="{ 'on-hover': hover }">
              <v-img
                :src="require('~/assets/images/SOne_index_bt-guarantee1.jpg')"
              >
              </v-img>
            </v-card>
          </v-hover>
        </v-col>
      </v-row>
    </v-col>
    <v-col>
      <v-row>
        <v-col cols="12" md="3" lg="3">
          <div class="head-search"><h3>ค้นหาศูนย์บริการใกล้บ้านคุณ</h3></div>
          <div class="box-search">
            <v-row>
              <v-col cols="12" class="">
                <v-col class="pa-1">
                  <v-row align="center">
                    <v-col cols="4" class="text-right">
                      <h4>จังหวัด</h4>
                    </v-col>
                    <v-col cols="8">
                      <v-select
                        dense
                        solo
                        hide-details
                        label="--เลือกกระทะล้อ--"
                      ></v-select>
                    </v-col>
                  </v-row>
                </v-col>
                <v-col class="pa-1">
                  <v-row align="center">
                    <v-col cols="4" class="text-right">
                      <h4>เขต/อำเภอ</h4>
                    </v-col>
                    <v-col cols="8">
                      <v-select
                        dense
                        solo
                        hide-details
                        label="--เลือกกระทะล้อ--"
                      ></v-select>
                    </v-col>
                  </v-row>
                </v-col>
                <v-col class="pa-1">
                  <v-row align="center">
                    <v-col cols="4" class="text-right">
                      <h4>ถนน</h4>
                    </v-col>
                    <v-col cols="8">
                      <v-select
                        dense
                        solo
                        hide-details
                        label="--เลือกกระทะล้อ--"
                      ></v-select>
                    </v-col>
                  </v-row>
                </v-col>
                <v-col class="pt-0 text-center">
                  <small style="color: red"
                    >หมายเหตุ : กรุณาเลือกอย่างใดอย่างหนึ่ง</small
                  >
                </v-col>
                <v-col class="pt-0">
                  <v-row align="center">
                    <v-col cols="4" class="text-right"> </v-col>
                    <v-col cols="8" class="text-center">
                      <v-btn color="#f05a28" small dark> ค้นหา </v-btn>
                    </v-col>
                  </v-row>
                </v-col>
              </v-col>
            </v-row>
          </div>
        </v-col>
        <v-col cols="12" md="5" lg="6">
          <div class="news-event">
            <div class="news-event-header">
              <v-col>
                <v-row class="pl-1 pr-1">
                  <h3>News & Events</h3>
                  <v-spacer></v-spacer>
                  <v-icon class="box" small color="#f05a28"
                    >mdi-checkbox-blank</v-icon
                  >
                  <v-icon class="box" small>mdi-checkbox-blank</v-icon>
                  <v-icon class="box" small>mdi-checkbox-blank</v-icon>
                </v-row>
              </v-col>
            </div>
            <v-col class="pb-6 pt-6">
              <v-row>
                <v-col
                  v-for="(item, i) in newsEvent"
                  :key="i"
                  cols="12"
                  md="4"
                  lg="4"
                >
                  <v-img :src="item.picture">
                    <div class="date-image">
                      <span> {{ item.date }} </span>
                    </div>
                  </v-img>
                  <div style="padding-top: 25px">
                    <span style="color: black">{{ item.detail }}</span>
                  </div>
                </v-col>
              </v-row>
            </v-col>
          </div>
        </v-col>
        <v-col cols="12" md="4" lg="3">
          <v-row>
            <v-col cols="5" class="pr-0">
              <v-img :src="require('~/assets/images/SOne_index_tips1.png')">
              </v-img>
            </v-col>
            <v-col cols="7" class="pl-0">
              <v-col style="background-color: black">
                <div class="text-center pt-1" v-if="mobile > 900">
                  <h4 style="color: red">Safety Tips</h4>
                </div>
                <div class="text-center pt-3" v-else>
                  <h2 style="color: red">Safety Tips</h2>
                </div>
                <div class="text-center" v-if="mobile > 900">
                  <small style="color: white; font-size: 11px"
                    >ควรเติมน้ำมันตอนเช้า ขณะที่อุณหภูมิบนพื้น ดินยังเย็นอยู่
                  </small>
                </div>
                <div class="text-center pb-3" v-else>
                  <span style="color: white; font-size: 16px"
                    >ควรเติมน้ำมันตอนเช้า ขณะที่อุณหภูมิบนพื้น ดินยังเย็นอยู่
                  </span>
                </div>
              </v-col>
            </v-col>
          </v-row>
          <v-row align="center">
            <v-col cols="5">
              <strong style="color: black">สมัครรับข่าวสาร</strong>
            </v-col>
            <v-col cols="7">
              <v-text-field
                dense
                outlined
                hide-details
                label="กรุณาใส่อีเมล์"
                color="#f05a28"
              ></v-text-field>
            </v-col>
          </v-row>
          <v-col>
            <div
              class="pt-2 mb-4"
              style="border-bottom: dashed 1px #f05a28"
            ></div>
            <v-img :src="require('~/assets/images/SOne_index_call.png')">
            </v-img>
          </v-col>
        </v-col>
      </v-row>
    </v-col>
  </div>
</template>

<script>
export default {
  name: "DefaultLayout",
  data() {
    return {
      mobile: false,
      newsEvent: [
        {
          detail:
            "ข่าวใหม่!! ข่าวและกิจกรรมข่าวและกิจกรรมข่าวและกิจกรรมข่าวและกิจกรรม",
          picture: require("@/assets/images/SOne_index_pic3.jpg"),
          date: "19 NOV 2014",
        },
        {
          detail:
            "ข่าวใหม่!! ข่าวและกิจกรรมข่าวและกิจกรรมข่าวและกิจกรรมข่าวและกิจกรรม",
          picture: require("@/assets/images/SOne_index_pic3.jpg"),
          date: "19 NOV 2014",
        },
        {
          detail:
            "ข่าวใหม่!! ข่าวและกิจกรรมข่าวและกิจกรรมข่าวและกิจกรรมข่าวและกิจกรรม",
          picture: require("@/assets/images/SOne_index_pic3.jpg"),
          date: "19 NOV 2014",
        },
      ],
    };
  },
  destroyed() {
    window.removeEventListener("resize", this.handleResize);
  },
  mounted() {
    window.addEventListener("resize", this.handleResize);
    this.handleResize();
  },
  methods: {
    handleResize() {
      this.mobile = window.innerWidth;
    },
  },
};
</script>
<style lang="scss">
h4 {
  color: white;
}
small {
  color: white;
}
.v-card {
  transition: opacity 0.4s ease-in-out;
}

.v-card:not(.on-hover) {
  opacity: 0.8;
  background-color: rgba(0, 0, 0, 1) !important;
}
.background {
  background-color: rgba(0, 0, 0, 1) !important;
}
.box:hover {
  color: #ff1e1e;
}
.date-image {
  color: white;
  background-color: black;
  width: 45px;
  font-size: 14px;
  text-align: center;
  margin-left: 10px;
}
</style>
