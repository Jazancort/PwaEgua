<template>
  <q-page class="flex flex-center">
    <img
      alt="Quasar logo"
      src="~assets/quasar-logo-full.svg"
    >
  </q-page>
</template>

<script>
export default {
  name: 'PageIndex'
}
</script>
<template>
  <q-page class="q-pt-sm">
    <div id="container">
      <div id="left"><select id="demoSelector"></select></div>
      <div id="middle"><img
          class="q-pa-sm q-pl-md q-pr-sm"
          alt="Trusty Icon"
          src="egua.png"
          width="120"
        ></div>
      <div id="right"><q-btn size="sm" id="runBtn">Executar</q-btn></div>
    </div>
    <q-separator
      size="2px"
      color="grey-13"
    />
    <div id="editor"></div>
    <div id="output" aria-live="polite"></div>
    <div>
    </div>
  </q-page>
</template>

<script>
export default {
  name: 'index'
}
</script>
