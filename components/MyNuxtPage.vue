<script setup>

</script>

<template>
  
  <v-layout class="overflow-visible" style="height: 56px;">
    <v-top-navigation

      active
      color="primary"
    >
      <v-btn>
        
        <NuxtLink to="/" class="n-link-base">
          <v-icon>mdi-home</v-icon>
          Home
        </NuxtLink>
      </v-btn>
      <v-btn>
        
        <NuxtLink to="/about" class="n-link-base">
          <v-icon>mdi-history</v-icon>
          About
        </NuxtLink>
      </v-btn>

      <v-btn>
        
        <NuxtLink to="/parent" class="n-link-base">
          <v-icon>mdi-heart</v-icon>
          Parent (index)
        </NuxtLink>
      </v-btn>

      <v-btn>
        
        <NuxtLink to="/parent/b" class="n-link-base">
          <v-icon>mdi-map-marker</v-icon>
          Parent (b)
        </NuxtLink>
      </v-btn>
      <v-btn class="n-link-base" @click="$router.push(`/parent/reload-${(Math.random() * 100).toFixed()}`)">
        Keyed child
      </v-btn>
      <v-btn class="n-link-base" @click="$router.push(`/parent/static-${(Math.random() * 100).toFixed()}`)">
        Non-keyed child
      </v-btn>
    </v-top-navigation>
    
  </v-layout>
  
  <v-container>
    <NuxtPage />
  </v-container>
</template>
