<template>
  <v-app>
    <headerContent class="mx-lg-auto mt-md-5 mt-lg-10 px-5 pt-5"/>
    <v-main>
      <mainContent class="mx-auto mb-5 mb-md-10 mb-lg-15"/>
    </v-main>
  </v-app>
</template>

<script>
import headerContent from '@/components/headerContent.vue';
import mainContent from '@/components/mainContent.vue';

export default {
  name: 'App',

  components: {
    headerContent,
    mainContent
  },

  data: () => ({
  //
  }),
}
</script>

<style lang="scss">
  .v-data-table {
    .v-data-table__wrapper  {
      table {
        thead {
          tr {
            th {
              font-size: 1rem !important;
            }
          }
        }
      }
    }
  }

  .v-data-table {
    .v-data-table__wrapper  {
      table {
        tbody {
          tr {
            td {
              font-size: calc(0.53rem + 0.55vmin) !important;
              margin: 0;
              padding-right: 0;
              line-height: 1;
            }
          }
        }
      }
    }
  }
</style>
