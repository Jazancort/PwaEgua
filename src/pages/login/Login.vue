<template>
  <q-page padding class="" style="background-color:white">
    <div class="">
      <div class="col-12 text-center">
        <q-btn flat :ripple="false" type="a" target="_blank" href="https://egua.tech/">
         <img
            class="q-pt-lg"
            alt="Egua Logo"
            src="eguatech.png"
            style="max-width: 8rem"
          >
        </q-btn>
      </div>
    </div>
    <carousel-info
      class="font_light col-8"
      style="font-size: 12px"
      :texts="textsCarousel"
    />

    <login-buttons />
    <p class="q-pt-lg text-center text-overline text-black q-pa-none q-ma-none">versão: {{ versionApp }}</p>
    <div class="text-center">
      <q-btn flat size="xs" :ripple="false" type="a" target="_blank" href="https://github.com/Jazancort">
        <q-icon name="fab fa-github">
          <p class="q-pt-md q-pl-sm text-right font_semi-bold text-black">Jazancort</p>
        </q-icon>
      </q-btn>
    </div>
  </q-page>
</template>

<script>
export default {
  name: 'PageLogin',
  components: {
    LoginButtons: () => import('components/login/LoginButtons'),
    CarouselInfo: () => import('components/carousel/CarouselInfo')
  },
  data () {
    return {
      textsCarousel: [
        'Programação simples, moderna e gratuita',
        'O Egua é uma Linguagem de Programação baseada em JavaScript, totalmente online e em português.',
        'Documentação completa e de fácil entendimento'
      ],
      versionApp: process.env.VERSION_APP
    }
  }
}
</script>
