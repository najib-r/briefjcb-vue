<template>
  <v-app>
    <headerContent class="text-center mx-lg-16"/>
    <v-main>
      <mainContent class="mx-auto mb-5"/>
    </v-main>
  </v-app>
</template>

<script>
import headerContent from './components/headerContent.vue';
import mainContent from './components/mainContent.vue';

export default {
  name: 'App',

  components: {
    headerContent,
    mainContent
  },

  data: () => ({
    //
  }),
};
</script>
