<template>
<div>
  <Nav/>
  <div>
    <LargeCardDisplay
        v-for="cardInfo in largeCardInfo.slice(0,1)"
        :key="cardInfo.id"
        :cardSection="cardInfo"
    />

    <SmallCardDisplay
        v-for="cardInfo in smallCardInfo"
        :key="cardInfo.id"
        :cardSection="cardInfo"
    />
  </div>
</div>
</template>

<script>
import { largeCardSections, smallCardSections } from "@/assets/data.js";
  export default {
    data () {
      return {
        largeCardInfo: largeCardSections,
        smallCardInfo: smallCardSections,
      }
    }
  }
</script>

<style scoped>

</style>
