<template>
<v-card>
  <v-card-title>
    <v-text-field
    v-model="search"
    append-icon="mdi-magnify"
    label="Search"
    single-line
    hide-details
    ></v-text-field>
  </v-card-title>
  <v-data-table
    :headers="headers"
    :items="jobs"
    :search="search"
    disable-pagination
    hide-default-footer
    dense>
    <template v-slot:[`item.name`]="{ item }">
      <a :href="item.link" class="links" target="_blank" rel="noopener noreferrer">{{ item.name }}</a>
  </template>
  </v-data-table>
</v-card>
</template>

<script>
export default {
    name: 'mainContent',
    data () {
        return {
            search: '',
            jobs: [
                {name: 'job 1', company: 'company 1', salary: '$ salary', link: 'https://google.com'},
                {name: 'job 2', company: 'company 2', salary: '$ salary', link: 'https://google.com'},
                {name: 'job 3', company: 'company 3', salary: '$ salary', link: 'https://google.com'},
                {name: 'job 4', company: 'company 4', salary: '$ salary', link: 'https://google.com'},
                {name: 'job 5', company: 'company 5', salary: '$ salary', link: 'https://google.com'},
                {name: 'job 6', company: 'company 6', salary: '$ salary', link: 'https://google.com'},
                {name: 'job 7', company: 'company 7', salary: '$ salary', link: 'https://google.com'},
                {name: 'job 8', company: 'company 8', salary: '$ salary', link: 'https://google.com'},
                {name: 'job 9', company: 'company 9', salary: '$ salary', link: 'https://google.com'},
                {name: 'job 10', company: 'company 10', salary: '$ salary', link: 'https://google.com'},
                {name: 'job 11', company: 'company 11', salary: '$ salary', link: 'https://google.com'},
            ],
            headers: [
                {
                  text: 'Job position',
                  align: 'left',
                  sortable: true,
                  value: 'name',
                },
                { text: 'Company', value: 'company'},
                { text: 'Salary', value: 'salary', sortable: false}
            ]
        }
    },
    methods: {
      redirectToLink: function(item) {
        window.open(item.link, '_blank');
      }
    }

}
</script>

<style scoped>
a {
    text-decoration: none;
}

a:link {
    color: #265301;
}
a:visited {
    color: #551A8B;
}

.links::before {
    content: "";
    display: block;
    position: absolute;
    left: 0;
    width: 100%;
    height: 1.5em;
}
</style>