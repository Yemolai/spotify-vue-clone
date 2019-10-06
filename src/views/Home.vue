<template>
  <v-container>
    <v-row>
      <v-col>
        <h1 class="view-title">
          Início
        </h1>
      </v-col>
    </v-row>
    <v-row v-for="section in sections" :key="section.id">
      <v-col>
        <list-section :section="section"/>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import { VCol, VContainer, VRow } from 'vuetify'
import ListSection from '@/components/ListSection'

export default {
  name: 'home',
  components: {
    ListSection,
    VCol,
    VContainer,
    VRow
  },
  data: function () {
    return {
      sections: [
        {
          name: 'Recently Played',
          playlists: [
            { type: 'playlist', spotifyMade: true, title: 'No Repeat', subtitle: 'As músicas que você não para de ouvir.', followers: 1 },
            { type: 'playlist', spotifyMade: true, title: 'De volta pro repeat', subtitle: 'As músicas que você costumava ouvir sem parar.', followers: 1 },
            { type: 'playlist', title: 'Músicas que você salvou', noOptions: true },
            { type: 'playlist', private: true, title: 'Rockstar Rádio', followers: 1 },
            { type: 'album', title: 'Jesus Is King - Kanye West (Album)', followers: 8764 },
            { type: 'album', title: 'Synthwave | Retro | 80s Vaporwave', subtitle: 'Best Synthwave playlist with the best Dark Synth Wave | Outrun | perehuaeiuah | japanese hiragana talk', followers: 36885 },
            { type: 'album', title: 'NINE', subtitle: 'blink-182' },
            { type: 'artist', name: 'Shinedown' }
          ]
        }
      ]
    }
  }
}
</script>
