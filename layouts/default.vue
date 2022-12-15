<template>
  <v-app dark>
    <v-navigation-drawer
      v-model="drawer"
      :clipped="clipped"
      fixed
      app
    >
      <v-list rounded class="mt-5">
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
          color="primary"
        >
          <v-list-item-action>
            <v-icon color="primary">{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar :clipped-left="clipped" fixed app elevation="0">
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-toolbar-title class="blue--text font-weight-bold">{{ title }}</v-toolbar-title>
      <v-spacer />
     <div class="me-4">
        <v-menu v-model="showProfile" max-width="500" offset-y>
          <template #activator="{ on, attrs }">
            <v-btn color="primary"  fab small dark v-bind="attrs" v-on="on">
              <v-badge dot overlap color="success">
                <v-btn icon>
                  <v-icon color="white">mdi-account-outline</v-icon></v-btn
                >
              </v-badge>
            </v-btn>
          </template>
          <v-card>
            <v-list>
              <v-list-item link>
                <v-btn icon color="primary"
                  ><v-icon>mdi-account-outline</v-icon></v-btn
                >
                <v-card-text>Account Info </v-card-text>
              </v-list-item>
              <v-list-item link>
                <v-btn icon color="primary"
                  ><v-icon>mdi-cog-outline</v-icon></v-btn
                >
                <v-card-text>Settings </v-card-text>
              </v-list-item>
              <v-list-item link>
                <v-btn icon color="primary"
                  ><v-icon>mdi-bell-outline</v-icon></v-btn
                >
                <v-card-text>Notifications </v-card-text>
              </v-list-item>
              <v-list-item link>
                <v-btn icon color="primary"><v-icon>mdi-power</v-icon></v-btn>
                <v-card-text>Logout </v-card-text>
              </v-list-item>
            </v-list>
          </v-card>
        </v-menu>
     </div>
    </v-app-bar>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    <v-footer :absolute="!fixed" app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Dashboard',
          to: '/',
        },
        {
          icon: 'mdi-account-group-outline',
          title: 'Manage',
          to: '/manage',
        },
         {
          icon: 'mdi-human-male-board-poll',
          title: 'Teachers',
          to: '/teacher',
        },
         {
          icon: 'mdi-chat-outline',
          title: 'Chats',
          to: '/chat',
        },
         {
          icon: 'mdi-chart-timeline-variant-shimmer',
          title: 'Lastest Activity',
          to: '/activity',
        },
        {
          icon: 'mdi-school-outline',
          title: 'Rooms',
          to: '/rooms',
        },
         {
          icon: 'mdi-new-box',
          title: 'News',
          to: '/new',
        },
        
      ],
      title: 'School Admin Dashboard',
      showProfile:false
    }
  },
}
</script>
