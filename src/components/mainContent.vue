<template>
  <v-card id="contentBox" fill-height>
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
    disable-sort
    hide-default-footer
    mobile-breakpoint="0"
    dense 
    id="myTable">
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
      jobs: [],
      headers: [
        {
          text: 'Job position',
          align: 'left',
          sortable: true,
          value: 'name',
          width: '20%'
        },
        { text: 'Company', value: 'company', width: '20%', align: 'left'},
        { text: 'Salary', value: 'salary', sortable: false, width: '10%', align:'left'}
      ]
    }
  },
  methods: {
    fetchJobs: function () {
      for (let i = 1; i < 76; i++) {
        let job = {name: `job really long job title ${i}`, company: `company really long company name ${i}`, salary: '$ salary', link:'https://google.com'}
        this.jobs.push(job);
      }
    }
  },
  created () {
    this.fetchJobs()
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

#contentBox {
  width: 95%;
  max-width: 900px;
}

@media only screen and (min-width: 768px) {
#contentBox {
  width: 50%;
}
}
</style>