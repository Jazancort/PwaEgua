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
              narrow-indicator
              switch-indicator
              active-color="primary"
              content-class="custom-tab"
            >
              <q-route-tab
              class="font_bold"
              style="font-size: 12px"
              no-caps to="/dashboard"
              >
                <q-icon size="1rem" name="fas fa-home" />
                Início
              </q-route-tab>
              <q-route-tab
              class="font_bold"
              style="font-size: 12px"
              no-caps to="/busca"
              >
                <q-icon size="1rem" name="fas fa-search" />
                Busca
              </q-route-tab>
              <q-route-tab
              class="font_bold"
              style="font-size: 12px"
              no-caps to="/seguros"
              >
                <q-icon size="1rem" name="fas fa-shield-alt" />
                Seguros
              </q-route-tab>
              <q-route-tab
              class="font_bold"
              style="font-size: 12px"
              no-caps to="/duvidas"
              >
                <q-icon size="1rem" name="fas fa-question" />
                Dúvidas
              </q-route-tab>
              <q-route-tab
              class="font_bold"
              style="font-size: 12px"
              no-caps
              to="/perfil"
              >
                <q-icon size="1rem" name="fas fa-user" />
                Perfil
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
