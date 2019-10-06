<template>
  <spotify-item :title="title" :subtitle="subtitle">
    <template v-slot="cover">
      <v-img :src="coverImage"/>
    </template>
  </spotify-item>
</template>

<script>
import SpotifyItem from '@/components/SpotifyItem'

export default {
  name: 'Playlist',
  components: {
    SpotifyItem
  },
  props: {
    title: {
      type: String,
      required: true
    },
    subtitle: String,
    followers: Number,
    coverImage: String
  }
}
</script>

<style>

</style>
