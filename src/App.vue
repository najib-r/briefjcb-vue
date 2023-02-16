<template>
  <v-app>
    <headerContent class="text-center mx-16 my-5"/>
    <v-main>
      <mainContent class="mx-16"/>
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
