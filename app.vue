<script setup>
const config = useAppConfig()
</script>

<template>
  <div> 
    <v-card>
      <v-layout>
        <v-app-bar title="Application bar"></v-app-bar>

        <v-navigation-drawer>
          <v-list>
            <v-list-item title="Navigation drawer"></v-list-item>
          </v-list>
        </v-navigation-drawer>

        <v-main>
          <v-container>
            <NuxtExampleLayout example="app-config">
              <h1 class="tet-h5">{{ config.title }}</h1>
              <p>{{ config.description }}</p>
              <v-btn v-if="config.showButton" prepend-icon="mdi-vuetify" variant="tonal">
                Button
              </v-btn>
            </NuxtExampleLayout>
          </v-container>
        </v-main>
      </v-layout>
    </v-card>
  </div>
</template>