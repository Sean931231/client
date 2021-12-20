<template>
  <div class="container">
    <HeroComponents />
    <div style="height: 150px"></div>
    <LargeCardDisplay
      v-for="cardInfo in largeCardInfo"
      :key="cardInfo.id"
      :cardSection="cardInfo"
    />
  </div>
</template>

<script>
import HeroComponents from '~/components/HeroComponents.vue'
import LargeCardDisplay from '~/components/LargeCardDisplay.vue'
import { largeCardSections } from '@/assets/data.js'

export default {
  name: 'IndexPage',
  components: { HeroComponents, LargeCardDisplay },
  data () {
    return {
      largeCardInfo: largeCardSections
    }
  }
}
</script>
