<template>
  <q-layout view="lHh Lpr lFf">
    <q-footer  class="transparent">
      <q-toolbar class="q-pa-none q-ma-none" style="min-height: 0px !important;">
        <q-toolbar-title rounded class="shadow-up-1 border-page">
          <!-- <div class="" > -->
            <q-tabs
              align="justify"
              no-caps
              class="text-grey-8 font_bold"
              switch-indicator
              active-color="purple-14"
              content-class="custom-tab"
            >
              <q-route-tab
              class="font_bold"
              style="font-size: 12px"
              no-caps to="/dashboard"
              >
                <q-icon class="q-pb-xs" size="1rem" name="fas fa-horse-head" />
                <!-- <img
                    class="q-pb-sm q-pr-sm"
                    alt="Trusty Icon"
                    src="eguatechnoname.png"
                    width="25"
                  > -->
                IDEgua
              </q-route-tab>
              <q-route-tab
              class="font_bold"
              style="font-size: 12px"
              no-caps to="/busca"
              >
                <q-icon class="icon-flipped q-pb-xs" size="1rem" name="fas fa-horse-head" />
                <!-- <img
                  class="q-pb-sm q-pr-sm"
                  alt="Trusty Icon"
                  src="eguatechPB.png"
                  width="25"
                > -->
                Documentação
              </q-route-tab>
            </q-tabs>
          <!-- </div>  -->
        </q-toolbar-title>
      </q-toolbar>
    </q-footer>

    <q-page-container class="bg-grey-2">
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
export default {
  name: 'MainLayout',
  data () {
    return {
      leftDrawerOpen: false
    }
  }
}
</script>
