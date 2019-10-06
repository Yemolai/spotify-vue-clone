<template>
  <div class="side">
    <div class="menus">
      <v-list dark>
        <v-list-item-group>
          <v-list-item>
            <v-list-item-icon>
              <v-icon dark>
                fas fa-ellipsis-h
              </v-icon>
            </v-list-item-icon>
          </v-list-item>
        </v-list-item-group>
        <v-list-item-group>
          <v-list-item v-for="(menu, k) in menus" :key="k">
            <v-list-item-icon>
              <v-icon dark>{{menu.icon}}</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title v-text="menu.label"/>
            </v-list-item-content>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </div>
    <div class="playlists">
      <user-playlists />
    </div>
  </div>
</template>

<script>
import UserPlaylists from '@/components/UserPlaylists'

export default {
  name: 'LeftSideLayout',
  components: { UserPlaylists },
  data: () => ({
    menus: [
      { icon: 'fas fa-home', label: 'Início' },
      { icon: 'fas fa-compact-disc', label: 'Navegar' },
      { icon: 'fas fa-satellite-dish', label: 'Rádio' }
    ]
  })
}
</script>
<style lang="scss" scoped>
.side {
  display: flex;
  flex-direction: column;
  padding: 0;
  margin: 0;
}
.menus {
  padding: 0 1em;
}
</style>
