<template>
  <v-app dark>
    <v-navigation-drawer
      v-model="drawer"
      mini-variant
      clipped
      permanent
      expand-on-hover
      fixed
      app
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar
      clipped-left
      fixed
      app
    >
      <div class="tw-flex tw-justify-between tw-items-center tw-w-full tw-px-1">
        <v-toolbar-title v-text="title" />
        <v-btn
          icon
          @click.stop="rightDrawer = !rightDrawer"
        >
          <v-icon>mdi-logout-variant</v-icon>
        </v-btn>
      </div>
    </v-app-bar>
    <v-main>
      <Nuxt />
    </v-main>
  </v-app>
</template>

<script>
import { navbars } from '~/config/navbar-menu'

export default {
  name: 'DefaultLayout',
  data () {
    return {
      drawer: false,
      items: navbars,
      title: 'Vuetify.js'
    }
  }
}
</script>
