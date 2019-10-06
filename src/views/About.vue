<template>
  <v-container>
    <v-row>
      <v-col>
        <h1 class="title">
          Spotify Desktop Client Vue Clone
        </h1>
        <p class="subtitle">
          Sobre este projeto
        </p>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <p>
          Este clone do Spotify tem como intuito demonstrar minhas habilidades
          como desenvolvedor front-end com Vue utilizando frameworks diversos e
          desenvolvendo rapidamente produtos de qualidade visual e de código
          com alta fidelidade à referência visual fornecida.
        </p>
        <p>
          Sou Romulo Gabriel Rodrigues, desenvolvedor Fullstack com especialização
          em JavaScript e web, com grande gosto por React e Vue.
        </p>
        <p>
          Se interessou e quer minhas habilidades à sua disposição? Entre em
          contato através do email contato@romulogabriel.com ou pelo
          <a :href="twitterLink">twitter</a>.
        </p>
      </v-col>
    </v-row>
  </v-container>
</template>
<script>
import { VContainer, VRow, VCol } from 'vuetify'

export default {
  name: 'AboutPage',
  components: { VContainer, VRow, VCol },
  data: () => ({
    twitterLink: 'https://twitter.com/yemolai'
  })
}
</script>
<style lang="scss" scoped>

</style>
