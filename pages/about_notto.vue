<template>
  <v-card class="overflow-hidden">
    <v-app-bar
      absolute
      dark
      prominent
      src="https://picsum.photos/1920/1080?random"
      scroll-target="#scrolling-techniques-4"
    >
      <template v-slot:img="{ props }">
        <v-img
          v-bind="props"
          gradient="to top right, rgba(100,115,201,.6), rgba(25,32,72,.6)"
        ></v-img>
      </template>

      <v-btn icon color=light-green large=true target="_blank" href="http://www.google.com"><v-icon>mdi-android</v-icon></v-btn>

      <v-toolbar-title>Paniti Achararit</v-toolbar-title>

      <v-spacer></v-spacer>

      <form action="https://www.google.com/search" class="searchform" method="get" name="searchform" target="_blank">
      <input name="sitesearch" type="hidden" value="">
      <input autocomplete="on" class="form-control search" name="q" placeholder="Type search" required="required"  type="text">
      <v-btn icon class="button" type="submit">
        <v-icon>mdi-magnify</v-icon>
      </v-btn>
      </form>

      <v-btn icon v-on:click="click=!click">
        <v-icon v-if="click" color=red >mdi-heart</v-icon>
        <v-icon v-else>mdi-heart</v-icon>
      </v-btn>

      <!-- <v-menu
        bottom
        left
      >
        <template v-slot:activator="{ on }">
          <v-btn
            icon
            color="yellow"
            v-on="on"
          >
            <v-icon>mdi-dots-vertical</v-icon>
          </v-btn>
        </template>

        <v-list>
          <v-list-item
            v-for="(item, i) in items"
            :key="i"
          >
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu> -->

      <template v-slot:extension>
        <v-tabs
          align-with-title
          background-color="transparent"
        >
          <v-tab :key="1" class="mycolor">My work</v-tab>
          <v-tab :key="2">Address</v-tab>
          <v-tab :key="3">Test...</v-tab>

          <v-tab-item :key="1">
            <v-card
              flat
              tile
            >
              <v-card-text><h1> My work </h1></v-card-text>
              <div id="app">
                <v-app id="inspire">
                      <v-row no-gutters class="mb-6" justify="center">
                        <v-column>
                          <v-hover>
                            <template v-slot:default="{ hover }">
                              <v-card
                                class="mx-auto"
                                max-width="344"
                              >
                                <v-img src="https://www.globalmagie.com/images/overlayimg/s3.jpg"></v-img>

                                <v-card-text>
                                  <h2 class="title primary--text">Global Magie</h2>
                                  Discover to the best instrument on planet Earth
                                </v-card-text>

                                <v-card-title>
                                  <v-rating
                                    :value="5"
                                    dense
                                    color="orange"
                                    background-color="orange"
                                    hover
                                    class="mr-2"
                                  ></v-rating>
                                  <span class="primary--text subtitle-2">32164 Reviews</span>
                                </v-card-title>

                                <v-fade-transition>
                                  <v-overlay
                                    v-if="hover"
                                    absolute
                                    color="#036358"
                                  >
                                    <v-btn href="http://www.globalmagie.com" target="_blank">See more info</v-btn>
                                  </v-overlay>
                                </v-fade-transition>
                              </v-card>
                            </template>
                          </v-hover>
                        </v-column>

                        <v-column>   <v-container style="width: 100px;"></v-container> </v-column>

                        <v-column>
                          <v-hover>
                            <template v-slot:default="{ hover }">
                              <v-card
                                class="mx-auto"
                                max-width="344"
                              >
                                <v-img src="https://www.thaiembassymnl.ph/images/stories/2018/WhatsNewTH/1.jpg"></v-img>

                                <v-card-text>
                                  <h2 class="title primary--text">Thai embassy manila</h2>
                                  Royal thai embassy in manila
                                </v-card-text>

                                <v-card-title>
                                  <v-rating
                                    :value="5"
                                    dense
                                    color="orange"
                                    background-color="orange"
                                    hover
                                    class="mr-2"
                                  ></v-rating>
                                  <span class="primary--text subtitle-2">99999 Reviews</span>
                                </v-card-title>

                                <v-fade-transition>
                                  <v-overlay
                                    v-if="hover"
                                    absolute
                                    color="#036358"
                                  >
                                    <v-btn href="http://www.thaiembassymnl.ph/en/" target="_blank">See more info</v-btn>
                                  </v-overlay>
                                </v-fade-transition>
                              </v-card>
                            </template>
                          </v-hover>
                        </v-column>
                      </v-row>
                </v-app>
              </div>
            </v-card>
          </v-tab-item>

          <v-tab-item :key="2">
            <v-card
              flat
              tile
            >
              <v-card-text><h1>This is where I work</h1></v-card-text>
              <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d12975.540960754935!2d139.68092895!3d35.6058973!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x6018f531259985c7%3A0x23bc8c6c2650ce38!2sSouth%20Building%203%2C%201-ch%C5%8Dme-31%20Ishikawach%C5%8D%2C%20Ota%20City%2C%20T%C5%8Dky%C5%8D-to%20145-0061!5e0!3m2!1sen!2sjp!4v1573733517331!5m2!1sen!2sjp"
              width="600" height="450" align="middle" frameborder="0" style="border:0;" allowfullscreen=""></iframe>
            </v-card>
          </v-tab-item>

          <v-tab-item :key="3">
            <v-card
              flat
              tile
            >
              <v-card-text><h1>This is......fun</h1></v-card-text>
              <v-img
                height="100%"
                src="http://www.soccersuck.com/img/b/3140044800.gif"
              ></v-img>
            </v-card>
          </v-tab-item>

        </v-tabs>
      </template>
    </v-app-bar>

    <v-sheet
      <!-- id="scrolling-techniques-4"
      class="overflow-y-auto" -->
      max-height="600"
    >
      <v-container style="height: 600px;"></v-container>
    </v-sheet>

  </v-card>
</template>

<script>
export default {
  data: () => ({
      items: [
        { title: 'Click Me1' },
        { title: 'Click Me2' },
        { title: 'Click Me3' },
        { title: 'Click Me4' },
      ],
      disabled: false,
      absolute: false,
      openOnHover: false,
      value: false,
      closeOnClick: true,
      closeOnContentClick: true,
      offsetX: false,
      offsetY: true,
      click: false,
      overlay: false
    }),
}
</script>
