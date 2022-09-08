<template>
  <v-app id="inspire">

    <HeaderComponent @handleDrawer="drawer = !drawer"/>

    <side-bar-component :drawer="drawer"/>
    
    <v-main>
      <v-container
        class="py-8 px-6"
        fluid
      >
        <router-view></router-view>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import SideBarComponent from './components/SideBarComponent.vue';
  export default {
    data: () => ({
        cards: ["Today", "Yesterday"],
        drawer: true,
    }),
    components: { HeaderComponent, SideBarComponent }
}
</script>