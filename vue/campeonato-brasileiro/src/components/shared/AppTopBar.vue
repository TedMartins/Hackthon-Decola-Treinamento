<template>
  <div class="app-top-bar">
    <v-app-bar app color="green lighten-1" dense dark >
      <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>
      <v-toolbar-title>Campeonato Brasileiro 2020 ⚽</v-toolbar-title>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" absolute temporary>
      <v-list nav dense>
        <v-list-item-group
          v-model="group"
          active-class="green--text text--lighten-1"
        >
          <router-link to="/">
            <v-list-item>
              <v-list-item-icon>
                <v-icon>mdi-home</v-icon>
              </v-list-item-icon>
              <v-list-item-title>Início</v-list-item-title>
            </v-list-item>
          </router-link>

          <router-link to="/classificacao">
            <v-list-item>
              <v-list-item-icon>
                <v-icon>mdi-soccer</v-icon>
              </v-list-item-icon>
              <v-list-item-title>Classificação</v-list-item-title>
            </v-list-item>
          </router-link>

        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>

<script>
export default {
  name: 'AppTopBar',
  data: () => ({
    drawer: false,
    group: null,
  }),
};
</script>

<style scoped>
a {
  color: green;
  text-decoration: none;
}
</style>