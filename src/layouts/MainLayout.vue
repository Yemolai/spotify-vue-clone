<template>
  <v-container fluid>
    <v-row>
      <div class="col" :style="{ maxWidth: `${leftSideWidth}px` }">
        <left-side-layout/>
      </div>
      <div class="col">
        <router-view/>
      </div>
      <div class="col" :style="{ maxWidth: `${rightSideWidth}px` }">
        <right-side-layout/>
      </div>
    </v-row>
    <v-footer dark>
      <music-player/>
    </v-footer>
  </v-container>
</template>

<script>
import LeftSideLayout from './LeftSideLayout'
import RightSideLayout from './RightSideLayout'
import MusicPlayer from '@/components/MusicPlayer'

export default {
  name: 'MainLayout',
  components: {
    LeftSideLayout,
    MusicPlayer,
    RightSideLayout
  },
  data: function () {
    return {
      leftSideWidth: 245,
      rightSideWidth: 400
    }
  }
}
</script>

<style lang="scss" scoped>
div.container {
  padding: 0;
  height: calc(100vh - 87px);
}
.col {
  padding: 0;
  margin: 0;
}
.col .side {
  background-color: rgb(66, 66, 66);
}
footer.theme--dark.v-sheet.v-footer {
  background-color: rgb(40, 40, 40);
  color: white;
  height: 87px;
  padding-bottom: 0;
  padding-top: 0;
  margin: 0;
  display: flex;
  justify-content: space-between;
}
</style>
