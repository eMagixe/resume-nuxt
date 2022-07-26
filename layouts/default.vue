<template>
  <v-app dark>
    <v-navigation-drawer v-model="drawer" :clipped="clipped" fixed app>
      <v-list-item two-line>
        <v-list-item-avatar>
          <img src="/images/personal/avatar.jpeg" />
        </v-list-item-avatar>

        <v-list-item-content>
          <v-list-item-title>Евченко Максим</v-list-item-title>
          <v-list-item-subtitle>Front-End Developer</v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>
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
    <v-app-bar :clipped-left="clipped" fixed app>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
    </v-app-bar>
    <v-main>
      <v-container fluid>
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
  name: "DefaultLayout",
  data() {
    return {
      clipped: true,
      drawer: true,
      fixed: true,
      items: [
        {
          icon: "mdi-home-outline",
          title: "Главная",
          to: "/",
        },
        {
          icon: "mdi-playlist-check",
          title: "Навыки",
          to: "/stack",
        },
        {
          icon: "mdi-briefcase-outline",
          title: "Опыт работы",
          to: "/experience",
        },
        {
          icon: "mdi-eye-arrow-right-outline",
          title: "Демо",
          to: "/demo",
        },
        {
          icon: "mdi-forum",
          title: "Контакты",
          to: "/contacts",
        },
        {
          icon: "mdi-information-outline",
          title: "Обо мне",
          to: "/about",
        },
      ],
      title: "Евченко Максим",
    };
  },
};
</script>
