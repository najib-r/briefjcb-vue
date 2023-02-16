<template>
  <v-app>
    <headerContent class="ma-16 pa-16"/>
    <v-main>
    </v-main>
  </v-app>
</template>

<script>
import headerContent from './components/headerContent.vue';

export default {
  name: 'App',

  components: {
    headerContent
  },

  data: () => ({
    //
  }),
};
</script>
