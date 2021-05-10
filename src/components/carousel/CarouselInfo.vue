<template>
  <div class="row">
    <div class="col-12">
      <q-carousel
        v-model="slide"
        transition-prev="scale"
        transition-next="scale"
        swipeable
        animated
        padding
        arrows
        control-color="black"
        control-text-color="deep-purple-14"
        navigation
        navigation-icon="fas fa-minus"
        height="220px"
        class="text-black rounded-borders transparent"
      >
        <q-carousel-slide
          v-for="(carousel, index) in texts"
          :key="index"
          :name="index"
          class="column no-wrap flex-center"
        >
          <div class="q-mt-md text-center font_bold" style="font-size: 13px;">
            {{ carousel }}
          </div>
        </q-carousel-slide>
      </q-carousel>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CarouselInfo',
  props: {
    texts: {
      type: Array,
      required: true,
      default: () => []
    }
  },
  data () {
    return {
      slide: 0,
      lorem: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Itaque voluptatem totam, architecto cupiditate officia rerum, error dignissimos praesentium libero ab nemo.'
    }
  }
}
</script>
