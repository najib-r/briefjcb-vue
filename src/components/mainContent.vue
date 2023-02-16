<template>
    <v-simple-table dense fixed-header height="300px">
      <template v-slot:default>
        <thead>
          <tr>
            <th class="text-subtitle-1 font-weight-bold">
              Job position
            </th>
            <th class="text-subtitle-1 font-weight-bold">
              Company
            </th>
            <th class="text-subtitle-1 font-weight-bold">
              Salary
            </th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="job in jobs" :key="job.name">
            <td><a :href="job.link" class="links" target="_blank" rel="noopener noreferrer">{{ job.name }}</a></td>
            <td>{{ job.company }}</td>
            <td>{{ job.salary }}</td>
          </tr>
        </tbody>
      </template>
    </v-simple-table>
  </template>

<script>
export default {
    name: 'mainContent',
    data () {
        return {
            jobs: [
                {name: 'job 1', company: 'company 1', salary: '$ salary', link: 'https://google.com'},
                {name: 'job 2', company: 'company 2', salary: '$ salary', link: 'https://google.com'},
                {name: 'job 3', company: 'company 3', salary: '$ salary', link: 'https://google.com'},
                {name: 'job 4', company: 'company 4', salary: '$ salary', link: 'https://google.com'}
            ]
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