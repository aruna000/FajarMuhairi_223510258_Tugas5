<template>
  <div class="q-pa-md">
    <q-layout
      view="lHh lpr lFf"
      container
      style="height: 1000px"
      class="shadow-2 rounded-borders"
    >
      <q-header elevated class="bg-deep-purple-2">
        <q-toolbar>
          <q-btn flat round dense src="/public/valo1.jpg" />
          <q-toolbar-title>Valo Shop</q-toolbar-title>

          <q-space />
        </q-toolbar>

        <q-toolbar inset>
          <q-breadcrumbs active-color="white" style="font-size: 16px">
            <q-breadcrumbs-el label="Home" icon="home" />
            <q-space />
            <q-breadcrumbs-el label="Transaksi" icon="widgets" />
            <q-space />
            <q-breadcrumbs-el label="History" />
          </q-breadcrumbs>
        </q-toolbar>
      </q-header>

      <q-page-container>
        <q-page class="q-pa-md">
          <!--awal dari carousel-->
          <div class="q-pa-md">
            <q-carousel
              v-model="slide"
              transition-prev="slide-right"
              transition-next="slide-left"
              swipeable
              animated
              control-color="red-8"
              navigation
              padding
              arrows
              height="300px"
              class="bg-grey-9 shadow-2 rounded-borders"
            >
              <q-carousel-slide :name="1" class="column no-wrap">
                <div
                  class="row fit justify-start items-center q-gutter-xs q-col-gutter no-wrap"
                >
                  <q-img
                    class="rounded-borders col-6 full-height"
                    src="/valo2.jpg"
                  />
                  <q-img
                    class="rounded-borders col-6 full-height"
                    src="/valo3.jpg"
                  />
                </div>
              </q-carousel-slide>
              <q-carousel-slide :name="2" class="column no-wrap">
                <div
                  class="row fit justify-start items-center q-gutter-xs q-col-gutter no-wrap"
                >
                  <q-img
                    class="rounded-borders col-6 full-height"
                    src="/valo4.jpg"
                  />
                  <q-img
                    class="rounded-borders col-6 full-height"
                    src="/valo5.jpg"
                  />
                </div>
              </q-carousel-slide>
            </q-carousel>
          </div>
          <!--akhir dari carousel-->

          <!--awal dari card-->
          <div class="q-pa-md row items-start q-gutter-md">
            <q-card class="my-card bg-deep-purple-2 text-white">
              <q-card-section>
                <q-img
                  class="rounded-borders col-6 full-height"
                  src="/point.png"
                />
                <div class="text-subtitle2 text-center">125 Points</div>
                <div class="text-subtitle2 text-center">Rp.14.000</div>
              </q-card-section>

              <q-card-section>
                {{ lorem }}
              </q-card-section>

              <q-separator dark />

              <q-card-actions vertical align="center">
                <q-btn
                  no-caps
                  unelevated
                  color="deep-purple-2"
                  @click="triggerNegative"
                  label="BELI"
                />
              </q-card-actions>
            </q-card>

            <q-card class="my-card bg-deep-purple-2 text-white">
              <q-card-section>
                <q-img
                  class="rounded-borders col-6 full-height"
                  src="/point.png"
                />
                <div class="text-subtitle2 text-center">420 Points</div>
                <div class="text-subtitle2 text-center">Rp.46.000</div>
              </q-card-section>

              <q-card-section>
                {{ lorem }}
              </q-card-section>

              <q-separator dark />

              <q-card-actions vertical align="center">
                <q-btn
                  no-caps
                  unelevated
                  color="deep-purple-2"
                  @click="triggerNegative"
                  label="BELI"
                />
              </q-card-actions>
            </q-card>

            <q-card class="my-card bg-deep-purple-2 text-white">
              <q-card-section>
                <q-img
                  class="rounded-borders col-6 full-height"
                  src="/point.png"
                />
                <div class="text-subtitle2 text-center">1375 Points</div>
                <div class="text-subtitle2 text-center">Rp.136.000</div>
              </q-card-section>

              <q-card-section>
                {{ lorem }}
              </q-card-section>

              <q-separator dark />

              <q-card-actions vertical align="center">
                <q-btn
                  no-caps
                  unelevated
                  color="deep-purple-2"
                  @click="triggerNegative"
                  label="BELI"
                />
              </q-card-actions>
            </q-card>

            <q-card class="my-card bg-deep-purple-2 text-white">
              <q-card-section>
                <q-img
                  class="rounded-borders col-6 full-height"
                  src="/point.png"
                />
                <div class="text-subtitle2 text-center">2400 Points</div>
                <div class="text-subtitle2 text-center">Rp.226.000</div>
              </q-card-section>

              <q-card-section>
                {{ lorem }}
              </q-card-section>

              <q-separator dark />

              <q-card-actions vertical align="center">
                <q-btn
                  no-caps
                  unelevated
                  color="deep-purple-2"
                  @click="triggerNegative"
                  label="BELI"
                />
              </q-card-actions>
            </q-card>
          </div>
          <!--akhir dari card-->
          <q-footer elevated>
            <q-toolbar class="bg-deep-purple-2">
              <q-toolbar-title class="text-caption"
                >&#169; Fajar. All rigths reserved
              </q-toolbar-title>
            </q-toolbar>
          </q-footer>
        </q-page>
      </q-page-container>
    </q-layout>
  </div>
</template>

<script>
import { ref } from "vue";
import { useQuasar } from "quasar";

export default {
  setup() {
    const $q = useQuasar();
    return {
      tab: ref("images"),
      time: ref("10:56"),
      timeWithSeconds: ref("09:24:10"),
      slide: ref("style"),
      lorem: "",
      slide: ref(1),
      triggerNegative() {
        $q.notify({
          type: "negative",
          message: "STOK HABIS.",
        });
      },
    };
  },
};
</script>

<style lang="sass" scoped>
.my-card
  width: 100%
  max-width: 250px
</style>
