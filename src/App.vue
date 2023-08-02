<template>
  <div class="relative-position ">
    <q-layout view="lHh Lpr lFf" class="relative-position bg-red">
      <q-header elevated class="glossy">
        <q-toolbar>
          <!-- Logo  
          <q-avatar>
            <img src="https://cdn.quasar.dev/img/avatar.png">
          </q-avatar> -->
          <q-toolbar-title> physio </q-toolbar-title>

          <div>
            <q-btn
              class="menu_bar"
              flat
              @click="leftDrawerOpen = !leftDrawerOpen"
              aria-label="Menu"
              icon="menu"
            />
            <div class="row justify-evenly menu_content">
              <q-btn flat>About Us</q-btn>
              <q-btn flat>Our Services</q-btn>
              <q-btn flat>Contact Us</q-btn>
            </div>
          </div>
        </q-toolbar>
      </q-header>

      <q-drawer v-model="leftDrawerOpen" bordered class="bg-grey">
        <q-list style="height: 38%" class="q-mt-xl">
          <q-item clickable v-ripple class="q-mb-lg">
            <q-item-section avatar>
              <q-icon name="groups" class="header_icon" />
            </q-item-section>
            <q-item-section class="font_size_header"> About Us </q-item-section>
          </q-item>

          <q-item clickable v-ripple class="q-mb-lg">
            <q-item-section avatar>
              <q-icon name="psychology" class="header_icon" />
            </q-item-section>
            <q-item-section class="font_size_header">
              Our Services
            </q-item-section>
          </q-item>

          <q-item clickable v-ripple>
            <q-item-section avatar>
              <q-icon name="call" class="header_icon" />
            </q-item-section>
            <q-item-section class="font_size_header">
              Contact Us
            </q-item-section>
          </q-item>
        </q-list>
      </q-drawer>

      <q-page-container>
        <HomeView />
      </q-page-container>
    </q-layout>
    <div class="absolute-center q-mt-xl bg-white" style="left: 2%;">
      <q-icon name="facebook" class="text-h3"/>
    </div>
  </div>
</template>

<script>
import HomeView from "./views/HomeView.vue";
import { ref } from "vue";
export default {
  name: "LayoutDefault",

  components: {
    HomeView,
  },

  setup() {
    return {
      leftDrawerOpen: ref(false),
    };
  },
};
</script>
<style>
.font_size_header {
  font-size: large;
}
.header_icon {
  color: orange;
  font-size: 30px !important;
}
/* --Banner Content Right */
.banner_content {
  font-size: 36px;
  padding: 0 23px;
  color: white;
}
/* --Icon Cover */
body.screen--xs {
  /* --Header  */
  .menu_bar {
    display: block;
  }
  .menu_content {
    display: none;
  }
  /* Header */

  /* --Info after banner */
  .info_left {
    font-size: 16px;
  }
}
body.screen--sm {
  /* --Header  */
  .menu_bar {
    display: block;
  }
  .menu_content {
    display: none;
  }
  /* --Header  */

  /* --Info after banner */
  .info_left {
    font-size: 16px;
  }
}
body.screen--md {
  /* --Header  */
  .menu_bar {
    display: none;
  }
  /* --Header  */
  /* Banner */
  .banner_content {
    font-size: 46px;
    color: white;
  }
  /* Banner */

  /* --Info after banner */
  .info_left {
    font-size: 18px;
  }
}
body.screen--lg {
  /* --Header  */
  .menu_bar {
    display: none;
  }
  /* --Header  */
  /* Banner */
  .banner_content {
    font-size: 46px;
    color: white;
  }
  /* Banner */

  /* --Info after banner */
  .info_left {
    font-size: 20px;
  }
}
body.screen--xl {
  /* --Header  */
  .menu_bar {
    display: none;
  }
  /* --Header  */
  /* Banner */
  .banner_content {
    font-size: 46px;
    color: white;
  }
  /* Banner */

  /* --Info after banner */
  .info_left {
    font-size: 22px;
  }
}
</style>
