<template>
  <div class="tile-links">
    <div class="row center-xs">
      <div class="tile-container middle-xs center-xs row col-md-4 p15" v-for="tile in social_tiles">
        <tile-link :tile="tile" />
      </div>
    </div>
  </div>
</template>

<script>
import { mapGetters } from 'vuex'

import TileLink from './TileLink.vue'
export default {
  name: 'tile-links',
  computed: {
    ...mapGetters({
      social_tiles: 'social/getSocialTiles'
    })
  },
  components: {
    TileLink
  }
}
</script>

<style lang="scss" scoped>
</style>