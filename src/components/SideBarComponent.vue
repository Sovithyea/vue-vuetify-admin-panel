<template>
  <v-navigation-drawer
      v-model="drawer"
      app
    >

        <v-img src="https://scontent.fpnh4-1.fna.fbcdn.net/v/t39.30808-6/297195552_3332151327016681_3186431922006151453_n.jpg?stp=dst-jpg_p960x960&_nc_cat=103&ccb=1-7&_nc_sid=e3f864&_nc_eui2=AeFqVZ1JAK7BRDOM10vdwQkogy6ddI9hBs2DLp10j2EGzfunyTo69lF0qpWTcG2iqGVZVpHuoTOqkNeXMj8Taf8B&_nc_ohc=z4Kn9Faa4sUAX8R5LMZ&_nc_ht=scontent.fpnh4-1.fna&oh=00_AT_gnyRgMLhLBw3OS66FX5ZswwYOTyE6ZFseQUEKtbEjuw&oe=62F721B1" class="pa-4">
        <div class="text-center mt-5">
            <v-avatar
                class="mb-4"
                color="grey darken-1"
                size="64"
            >
                <v-img aspect-ratio="30" 
                src="https://ibccambodia.com/wp-content/uploads/freshizer/118f9493820a1203922af1029ad89adb_YG-logo-867-c-90.jpg">
                </v-img>
            </v-avatar>
            <h3 class="white--text">
                YAMATO GREEN CO., LTD.
            </h3>
        </div>        
        </v-img>
      <v-divider></v-divider>

      <v-list>
        <v-list-item
          v-for="[icon, text] in links"
          :key="icon"
          link
        >
          <v-list-item-icon>
            <v-icon>{{ icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ text }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

</template>

<script>
export default {
    props: [
        'drawer'
    ],
    data() {
        return {
            links: [
            ["mdi-view-dashboard", "Dashboard"],
            ["mdi-account", "Profile"],
            ["mdi-view-list", "Product"],
            ["mdi-clipboard-minus-outline", "Order"],
            ["mdi-cog-outline", "Setting"],
        ],
        }
    }
}
</script>

<style>

</style>