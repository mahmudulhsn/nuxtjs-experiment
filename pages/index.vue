<template>
  <div>
    <div class="container">
      <Hero />
      <LargeCardDisplay
        v-for="cardInfo in largecardInfo"
        :key="cardInfo.id"
        :cardSection="cardInfo"
      />
      <SmallCardDisplay
        v-for="cardInfo in smallcardInfo"
        :key="cardInfo.id"
        :cardSection="cardInfo"
      />
    </div>
  </div>
</template>

<script>
import { largeCardSections,  smallCardSections } from "@/assets/data.js";
export default {
  data () {
    return {
      largecardInfo: largeCardSections,
      smallcardInfo: smallCardSections
    }
  }
}
</script>
