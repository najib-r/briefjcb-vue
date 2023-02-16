<template>
    <v-simple-table dense fixed-header height="300px">
      <template v-slot:default>
        <thead>
          <tr>
            <th>
              Job position
            </th>
            <th>
              Company
            </th>
            <th>
              Salary
            </th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="job in jobs" :key="job.name">
            <td>{{ job.name }}</td>
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
                {name: 'job 1', company: 'company 1', salary: '$ salary'},
                {name: 'job 2', company: 'company 2', salary: '$ salary'},
                {name: 'job 3', company: 'company 3', salary: '$ salary'},
                {name: 'job 4', company: 'company 4', salary: '$ salary'}
            ]
        }
    }
}
</script>