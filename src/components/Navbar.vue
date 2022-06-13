<template>
  <div class="navbar-main">
    <!-- size lg -->
    <v-app-bar class="hidden-sm-and-down" color="white" fixed>
      <v-toolbar-items>
        <v-btn text to="/">
          <span class="mr-2">صفحه اصلی</span>
        </v-btn>
        <v-btn text to="/products">
          <span class="mr-2">دانلود آهنگ</span>
        </v-btn>
        <v-btn text to="/about">
          <span class="mr-2">موزیک ویدیو</span>
        </v-btn>

        <v-btn text to="/about">
          <span class="mr-2">دانلود آلبوم</span>
        </v-btn>

        <v-btn text to="/about">
          <span class="mr-2">سینما</span>
        </v-btn>

        <v-btn text to="/about">
          <span class="mr-2">گالری</span>
        </v-btn>

        <v-btn text to="/about">
          <span class="mr-2">پخش آثار</span>
        </v-btn>
        <v-menu open-on-hover offset-y>
          <template v-slot:activator="{ on, attrs }">
            <v-btn text v-bind="attrs" v-on="on"> ... </v-btn>
          </template>
          <v-list>
            <v-list-item>
              <v-list-item-title>هنرمندان</v-list-item-title>
            </v-list-item>

            <v-list-item>
              <v-list-item-title>متن آهنگ</v-list-item-title>
            </v-list-item>

            <v-list-item>
              <v-list-item-title>اینستا آرتیست</v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-list-item-title>دانلود اپلیکیشن</v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-list-item-title>تبلیغات درسابت</v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-list-item-title>درباره ما</v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-list-item-title>تماس باما</v-list-item-title>
            </v-list-item>
          </v-list>
        </v-menu>

        <span class="mr-3">
          <v-text-field
            v-model="message"
            append-icon="mdi-search-web"
            :prepend-icon="icon"
            filled
            placeholder="کلمه موردنظر را تایپ کنید"
            type="text"
            @click:append="sendMessage"
          ></v-text-field>
        </span>
      </v-toolbar-items>
      <v-spacer></v-spacer>

      <v-toolbar-items>
        <router-link to="/cart">
          <v-btn text>
            <v-icon class="mr-2">mdi-github</v-icon>
          </v-btn>
        </router-link>
      </v-toolbar-items>
    </v-app-bar>

    <!-- size mobile -->
    <v-app-bar class="hidden-sm-and-up" color="white" fixed>
      <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>
      <v-spacer></v-spacer>
      <span class="mt-2 mr-3">
        <v-text-field
          v-model="message"
          append-icon="mdi-search-web"
          :prepend-icon="icon"
          filled
          placeholder="کلمه موردنظر را تایپ کنید"
          type="text"
          @click:append="sendMessage"
        ></v-text-field>
      </span>
      <router-link to="/cart">
        <v-btn text>
          <v-icon class="mr-2">mdi-github</v-icon>
        </v-btn>
      </router-link>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" absolute temporary>
      <v-system-bar></v-system-bar>
      <v-list>
        <v-list-item>
          <v-list-item-avatar>
            <v-img
              src="https://lh3.googleusercontent.com/a-/AOh14GhRowOcRCeXt5Uw7plDEq6qacBrFbyjB-UQ7txUbw=s96-c-rg-br100"
            ></v-img>
          </v-list-item-avatar>
        </v-list-item>

        <v-list-item link>
          <v-list-item-content>
            <v-list-item-title class="text-h6"> محمد شریفی </v-list-item-title>
            <v-list-item-subtitle>amirpeace1080@gmail.com</v-list-item-subtitle>
          </v-list-item-content>

          <v-list-item-action>
            <v-icon>mdi-menu-down</v-icon>
          </v-list-item-action>
        </v-list-item>
      </v-list>
      <v-divider></v-divider>
      <v-list nav dense>
        <v-list-item-group color="primary">
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>
                <router-link to="/">صفحه اصلی</router-link>
              </v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>
                <router-link to="/products">دانلود آهنگ</router-link>
              </v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>
                <router-link to="/about">موزیک ویدیو</router-link>
              </v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>
                <router-link to="/about">دانلود آلبوم</router-link>
              </v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>
                <router-link to="/about">سینما</router-link>
              </v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>
                <router-link to="/about">گالری</router-link>
              </v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>
                <router-link to="/about">پخش آثار</router-link>
              </v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>
                <!-- <router-link to="/about">...</router-link> -->

                <v-list-group :value="true" no-action sub-group>
                  <template v-slot:activator>
                    <v-list-item-content>
                      <v-list-item-title>...</v-list-item-title>
                    </v-list-item-content>
                  </template>

                  <v-list-item link>
                    <v-list-item-title>هنرمندان</v-list-item-title>
                  </v-list-item>
                  <v-list-item link>
                    <v-list-item-title>متن آهنگ</v-list-item-title>
                  </v-list-item>
                  <v-list-item link>
                    <v-list-item-title>اینستا آرتیست</v-list-item-title>
                  </v-list-item>
                  <v-list-item link>
                    <v-list-item-title>دانلود اپلیکیشن</v-list-item-title>
                  </v-list-item>
                  <v-list-item link>
                    <v-list-item-title>تبلیغات در سایت</v-list-item-title>
                  </v-list-item>
                  <v-list-item link>
                    <v-list-item-title>درباره ما</v-list-item-title>
                  </v-list-item>
                  <v-list-item link>
                    <v-list-item-title>تماس باما</v-list-item-title>
                  </v-list-item>
                </v-list-group>
              </v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
      group: null,
    };
  },
  methods: {
    async sendMessage() {
      this.showSearch = true;
      await axios
        .get(
          `https://fakerestapi.azurewebsites.net/api/v1/Activities/${this.message}`
        )
        .then((res) => {
          this.resultSearch = res;
        });
    },
  },
};
</script>

<style scoped>
.navbar-main {
  margin-bottom: 50px;
}
</style>