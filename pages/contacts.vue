<template>
  <default-page
    title="Контакты"
    image="/images/pages/contacts.jpg"
    prev="/demo"
    next="/about"
  >
    <v-card-title>Связь</v-card-title>
    <v-list>
      <v-list-item-group>
        <v-list-item v-for="(item, i) in contacts" :key="i">
          <v-list-item-icon>
            <v-icon v-text="item.icon"></v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title>
              <a class="contact" :href="item.href">{{ item.text }}</a>
            </v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-item-group>
    </v-list>
    <v-card-title>Ссылки</v-card-title>
    <v-list>
      <v-list-item-group>
        <v-list-item v-for="(item, i) in links" :key="i">
          <v-list-item-icon>
            <v-icon v-text="item.icon"></v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title>
              <a class="contact" :href="item.href">{{ item.text }}</a>
            </v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-item-group>
    </v-list>
  </default-page>
</template>

<script>
export default {
  name: "ContactsPage",
  data: () => ({
    contacts: [
      {
        href: "tel:+79962552383",
        text: "+7 (996) 255-23-83",
        icon: "mdi-cellphone",
      },
      {
        href: "https://t.me/max_magixe",
        text: "@max_magixe",
        icon: "mdi-chat",
      },
      {
        href: "mailto:max.magixe@gmail.com",
        text: "max.magixe@gmail.com",
        icon: "mdi-email",
      },
    ],
    links: [
      {
        href: "https://github.com/eMagixe",
        text: "github.com/eMagixe",
        icon: "mdi-link-variant",
      },
      {
        href: "https://hh.ru/resume/55584c38ff0768026f0039ed1f70326b666538",
        text: "hh.ru",
        icon: "mdi-link-variant",
      },
      {
        href: "https://linkedin.com/in/max-magixe",
        text: "linkedin.com",
        icon: "mdi-link-variant",
      },
    ],
  }),
};
</script>

<style>
a.contact {
  text-decoration: none;
  color: cornflowerblue;
}
</style>
