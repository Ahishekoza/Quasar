<template>
  <div class="relative-position ">
    <q-layout view="lHh Lpr lFf" class="relative-position">
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
    <div class="fixed-center column  icon_position" >
      <q-icon name="facebook" class="text-h3 icon_color q-mb-sm"/>
      <q-icon name="facebook" class="text-h3 icon_color"/>
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
/* Social Media Icon Position*/
.icon_position{
  left: 3%;
  cursor: pointer;
}
.icon_color{
  background-color:white;
}
.icon_color:hover{
  background-color: brown;
  border-radius: 10px;
  color: white;
  transition: all 0.5s ease-in;

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

  /* Social Media Icon Position*/
.icon_position{
  display: none;
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

  /* Social Media Icon Position*/
.icon_position{
  left: 3%;
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

  /* Social Media Icon Position*/
.icon_position{
  left: 3%;

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
  .icon_position{
  left: 1%;
  cursor: pointer;
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
  .icon_position{
  left: 1%;
  cursor: pointer;
}
}
</style>
