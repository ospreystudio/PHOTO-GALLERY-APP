<template>
      <v-container fluid>
    <v-app-bar
     
      color="teal"
      dark
    >
    <v-spacer />
    <v-btn class="mx-2" ml-3>
        <router-link to='/'>main page</router-link>
    </v-btn>
        <v-btn ml-3>
        <router-link to='/photo'>Photo Gallery</router-link>
    </v-btn>

    </v-app-bar>  
</v-container>

</template>


<script>

export default {
    components: {

    }
}
</script>