<template>
  <div class="user-playlists">
    <v-list dark dense>
      <v-subheader class="list-title">
        Sua biblioteca
      </v-subheader>
      <v-list-item-group color="white">
        <v-list-item v-for="(playlist, k) in userLibrary" :key="`lib-${k}`">
          <v-list-item-content>
            <v-list-item-title>
              {{ playlist.title }}
            </v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-item-group>
      <v-subheader class="list title">
        Playlists
      </v-subheader>
      <v-list-item-group color="white">
        <v-list-item
          dark
          v-for="(playlist, k) in userPlaylists"
          :key="`playlist-${k}`">
          <v-list-item-content>
            <v-list-item-title>
              {{ playlist.title }}
              <span class="hover-details">
                <span v-if="playlist.from">
                  &middot; de {{ playlist.from }}
                </span>
                <span v-else-if="playlist.to">
                  &middot; para {{ playlist.from }}
                </span>
              </span>
            </v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-item-group>
    </v-list>
  </div>
</template>

<script>
export default {
  name: 'UserPlaylists',
  data: () => ({
    userLibrary: [
      { title: 'Feito pra você' },
      { title: 'Tocados recentemente' },
      { playing: true, title: 'Músicas curtidas' },
      { title: 'Álbuns' },
      { title: 'Artistas' },
      { title: 'Podcasts' }
    ],
    userPlaylists: [
      { title: 'de frente pro marzão', from: 'Isabelle Samways' },
      { title: 'De volta pro repeat', to: 'Romulo Gabriel Rodrigues' },
      { title: 'No Repeat', to: 'Romulo Gabriel Rodrigues' },
      { title: 'Rockstar Rádio', from: 'Spotify' },
      { title: 'Slack Rádio', from: 'Spotify' },
      { title: 'Rala e Rola', from: 'Spotify' },
      { title: 'At our feet', unseenUpdated: true },
      { title: 'CHINELADA', from: 'Fernando Muller' },
      { title: 'EmOxInHu *-*', from: 'Isabelle Samways', unseenUpdated: true },
      { title: 'Crossfire Rádio', from: 'Spotify' }
    ]
  })
}
</script>

<style>
.list-title {
  text-transform: uppercase;
  letter-spacing: 2px;
}
.hover-details {
  color: transparent;
}
.user-playlists {
  overflow-y: auto;
  max-height: 30vh;
  padding: 0 1em;
}

.hover-details:hover {
  color: white;
}
.v-list-item__icon {
  margin-right: 15px;
}
.v-list-item__title {
  align-self: flex-start;
  text-align: left;
}
</style>
