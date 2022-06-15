<template>
  <div>
    <v-card width="100%">
      <div>
        <div class="text-right">
          <v-card-subtitle>
            <span>آخرین مطالب</span>
            <v-icon style="float: left" color="info"
              >mdi-calendar-month-outline</v-icon
            >
          </v-card-subtitle>
          <div class="mr-7">
            <ol>
              <router-link to="/">
                <li class="mt-2 mb-1">
                  دانلود آهنگ علی منتظری خنده
                </li></router-link
              >
              <hr />
              <router-link to="/">
                <li class="mt-2 mb-1">
                  دانلود آهنگ سینا شعبانخانی یاردلم
                </li></router-link
              >
              <hr />

              <router-link to="/">
                <li class="mt-2 mb-1">
                  دانلود آهنگ رضا بهرام لیلا
                </li></router-link
              >
              <hr />
              <router-link to="/">
                <li class="mt-2 mb-1">
                  دانلود آهنگ محسن چاووشی قشنگ من
                </li></router-link
              >
              <hr />

              <router-link to="/">
                <li class="mt-2 mb-1">
                  دانلود آهنگ بابک جهانبخش تو منو کی کشتی
                </li></router-link
              >
              <hr />
              <router-link to="/">
                <li class="mt-2 mb-1">
                  دانلود آهنگ سون بند تقصیر من نیست
                </li></router-link
              >
              <hr />

              <router-link to="/">
                <li class="mt-2 mb-1">
                  دانلود آهنگ یوسف زمانی عشق منه
                </li></router-link
              >
              <hr />
              <router-link to="/">
                <li class="mt-2 mb-1">
                  دانلود آهنگ ناصر زینعلی با توام
                </li></router-link
              >
            </ol>
          </div>
        </div>
      </div>
    </v-card>

    <!-- card two -->

    <v-card class="mt-8" width="100%">
      <div>
        <div class="text-right">
          <v-card-subtitle>
            <span>در انتظار پخش</span>
            <v-icon style="float: left" color="info"
              >mdi-headphones</v-icon
            >
          </v-card-subtitle>
          <div class="mr-7">
            <ol>
              <router-link to="/">
                <li class="mt-2 mb-1">
                  دانلود آهنگ امیرتتلو حق
                </li></router-link
              >
              <hr />
              <router-link to="/">
                <li class="mt-2 mb-1">
                  دانلود آهنگ امیرتتلو بهت
                </li></router-link
              >
              <hr />

              <router-link to="/">
                <li class="mt-2 mb-1">
                  دانلود آهنگ مسیح و آرش AP برف
                </li></router-link
              >
              <hr />
              <router-link to="/">
                <li class="mt-2 mb-1">
                  دانلود آهنگ محسن چاووشی قشنگ من
                </li></router-link
              >
              <hr />

              <router-link to="/">
                <li class="mt-2 mb-1">
                  دانلود آهنگ رضا بهرام عاشقی درد قشنگیست
                </li></router-link
              >
              <hr />
              <router-link to="/">
                <li class="mt-2 mb-1">
                  دانلود آهنگ مهدی جهانی نمیفهمی تو آدمو
                </li></router-link
              >
              <hr />

              <router-link to="/">
                <li class="mt-2 mb-1">
                  دانلود آهنگ علیرضا پویا میخوامت دلی
                </li></router-link
              >
              <hr />
              <router-link to="/">
                <li class="mt-2 mb-1">
                  دانلود آهنگ مهراد جم نیست
                </li></router-link
              >
              <hr />
              <router-link to="/">
                <li class="mt-2 mb-1">
                  دانلود آهنگ آرون افشار چال گونه
                </li></router-link
              >
            </ol>
          </div>
        </div>
      </div>
    </v-card>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
li {
  list-style-type: none;
  font-size: 13px;
  color: #3e2723;
}
</style>