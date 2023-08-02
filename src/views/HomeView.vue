<template>
  <q-page>
    <!-- Banner Section -->
    <div>
      <q-parallax src="https://cdn.quasar.dev/img/parallax2.jpg">
        <div class="custom_width row">
          <div class="col-12 col-md-5 banner_content flex flex-center">
            Let Us Help You & Your Family To Maintain The Health
          </div>
          <div class="col-md-7 column flex-center gt-sm">
            <div class="border_card q-mb-md">About Us</div>
            <div class="border_card q-mb-md">Our Services</div>
            <div class="border_card">Contact Us</div>
          </div>
        </div>
      </q-parallax>
    </div>

    <!-- About us -->
    <div class="container q-mt-md row" style=" min-height: fit-content">
      <div class="col-12 col-md-6 col-lg-6 flex flex-center q-pa-md info_right">
        2022 marked 10 years delivering film and television production
        physiotherapy, osteopathy, on-set massage and health services to
        productions large and small
      </div>
      <div class="col-12 col-md-6 col-lg-6 flex flex-center q-pa-md info_left gt-sm">
        The Film Physios exists to keep productions productive. All our services
        can be delivered on set, on location, on call & in our on the lot
        clinics.
        <p></p>
        We provide physiotherapy/ vocal physiotherapy/ osteopathy/ on-set
        massage therapy/ transformational PT for talent/ to location clinics/
        24-7 concierge.
        <p></p>
        We operate across studios large and small, from Pinewood, Shepperton,
        Warner Bros Leavesden, Longcross and Sky Elstree to independent
        facilities across London and the South east
      </div>
    </div>

    <!-- Our Components -->
    <div class="q-mt-md bg-red q-px-md">
      <h4 class="text-center">Our Services</h4>
      <div class="row  ">
        <div class="col-12 col-md-4">
          <q-card class="my-card">
            <img src="https://cdn.quasar.dev/img/mountains.jpg">

            <q-card-section>
              <div class="text-h6">Our Changing Planet</div>
              <div class="text-subtitle2">by John Doe</div>
            </q-card-section>

            <q-card-section class="q-pt-none">
              {{ lorem }}
            </q-card-section>
          </q-card>
        </div>
        <div class="col-12 col-md-4">
          <q-card class="my-card">
            <img src="https://cdn.quasar.dev/img/mountains.jpg">

            <q-card-section>
              <div class="text-h6">Our Changing Planet</div>
              <div class="text-subtitle2">by John Doe</div>
            </q-card-section>

            <q-card-section class="q-pt-none">
              {{ lorem }}
            </q-card-section>
          </q-card>
        </div>
        <div class="col-12 col-md-4">
          <q-card class="my-card">
            <img src="https://cdn.quasar.dev/img/mountains.jpg">

            <q-card-section>
              <div class="text-h6">Our Changing Planet</div>
              <div class="text-subtitle2">by John Doe</div>
            </q-card-section>

            <q-card-section class="q-pt-none">
              {{ lorem }}
            </q-card-section>
          </q-card>
        </div>
        <div class="col-3">
          <q-card class="my-card">
            <img src="https://cdn.quasar.dev/img/mountains.jpg">

            <q-card-section>
              <div class="text-h6">Our Changing Planet</div>
              <div class="text-subtitle2">by John Doe</div>
            </q-card-section>

            <q-card-section class="q-pt-none">
              {{ lorem }}
            </q-card-section>
          </q-card>
        </div>
      </div>
    </div>
  </q-page>
</template>

<script>
export default {
  name: "HomeView",
};
</script>
<style>
/* Banner Content */
.custom_width {
  height: 300px;
  width: 100%;
}

/* Banner right Content */
.border_card {
  width: 560px;
  text-align: center;
  border: 1px solid white;
  padding: 10px 2px;
  font-size: x-large;
  font-weight: 600;
  color: white;
  cursor: pointer;
}

.border_card:hover {
  background-color: white;
  color: red;
  transition: all 0.5s ease-in;
}

/* Container Common Class */
.container {
  width: 80%;
  margin: 0 auto;
}

/* --Info Page Content Management */
.info_right {
  font-size: 30px;
  line-height: 35px;
}
/* Card Width */
.my_card{
  width: 100%;
  max-width: 250px;
}
</style>
