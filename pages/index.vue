<template>
  <b-table :data="data">
    <b-table-column field="id" label="ID" width="40" numeric v-slot="props">
      {{ props.row.id }}
    </b-table-column>
    <b-table-column field="first_name" label="First Name" v-slot="props">
      {{ props.row.first_name }}
    </b-table-column>
    <b-table-column field="last_name" label="Last Name" v-slot="props">
      {{ props.row.first_name }}
    </b-table-column>
    <b-table-column field="date" label="Date" centered v-slot="props">
      {{ props.row.date }}
    </b-table-column>
    <b-table-column field="gender" label="Gender" v-slot="props">
      {{ props.row.gender }}
    </b-table-column>
  </b-table>
</template>

<script>
export default {
  data() {
    return {
      data: [
        { 'id': 1, 'first_name': 'Jesse', 'last_name': 'Simmons', 'date': '2016-10-15 13:43:27', 'gender': 'Male' },
        { 'id': 2, 'first_name': 'John', 'last_name': 'Jacobs', 'date': '2016-12-15 06:00:53', 'gender': 'Male' },
        { 'id': 3, 'first_name': 'Tina', 'last_name': 'Gilbert', 'date': '2016-04-26 06:26:28', 'gender': 'Female' },
        { 'id': 4, 'first_name': 'Clarence', 'last_name': 'Flores', 'date': '2016-04-10 10:28:46', 'gender': 'Male' },
        { 'id': 5, 'first_name': 'Anne', 'last_name': 'Lee', 'date': '2016-12-06 14:38:38', 'gender': 'Female' }
      ],
      columns: [
        {
          field: 'id',
          label: 'ID',
          width: '40',
          numeric: true
        },
        {
          field: 'first_name',
          label: 'First Name',
        },
        {
          field: 'last_name',
          label: 'Last Name',
        },
        {
          field: 'date',
          label: 'Date',
          centered: true
        },
        {
          field: 'gender',
          label: 'Gender',
        }
      ]
    }
  }
}
</script>
