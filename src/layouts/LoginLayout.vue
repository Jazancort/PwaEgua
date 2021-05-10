<template>
  <q-layout view="lHh Lpr lFf">
    <q-page-container class="bg-primary" >
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>

export default {
  name: 'LoginLayout',
  data () {
    return {
      leftDrawerOpen: false
    }
  }
}
</script>
