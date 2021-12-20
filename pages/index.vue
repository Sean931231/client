<template>
  <div>
    <Nav />
    <div class="container">
      <HeroComponents />
      <div style="height: 150px" />
      <LargeCardDisplay
        v-for="cardInfo in largeCardInfo"
        :key="cardInfo.id"
        :cardSection="cardInfo"
      />
      <SmallCardDisplay
        v-for="cardInfo in smallCardSections"
        :key="cardInfo.id"
        :cardsSection="cardInfo"
      />
    </div>
  </div>
</template>

<script>
import HeroComponents from '~/components/HeroComponents.vue'
import LargeCardDisplay from '~/components/LargeCardDisplay.vue'
import Nav from '~/components/Nav.vue'
import { largeCardSections, smallCardSections } from '@/assets/data.js'

export default {
  name: 'IndexPage',
  components: { HeroComponents, LargeCardDisplay, Nav },
  data () {
    return {
      largeCardInfo: largeCardSections,
      smallCardSections
    }
  }
}
</script>
