<template>
  <div>
    <div class="blue--text text-h6 font-weight-bold mb-4">Manage Teacher</div>
    <div class="mt-10">
      <v-data-table
        :headers="headers"
        :items="desserts"
        :items-per-page="5"
        class="elevation-3"
      >
        <template #[`item.Action`]>
          <v-tooltip top color="error">
            <template #activator="{ on, attrs }">
              <v-btn icon v-bind="attrs" v-on="on">
                <v-icon color="error">mdi-trash-can-outline</v-icon>
              </v-btn>
            </template>
            <span>Delete</span>
          </v-tooltip>
          <v-tooltip top color="primary">
            <template #activator="{ on, attrs }">
              <v-btn icon v-bind="attrs" v-on="on">
                <v-icon color="primary">mdi-pencil-outline</v-icon>
              </v-btn>
            </template>
            <span>Edit</span>
          </v-tooltip>
        </template>
        <template #[`item.Image`]>
          <v-avatar>
            <v-img src="https://cdn.vuetifyjs.com/images/john.jpg" />
          </v-avatar>
        </template>
      </v-data-table>
    </div>
  </div>
</template>

<script>
export default {
  name: 'InspirePage',
  data() {
    return {
      headers: [
        { text: 'Image', value: 'Image' },

        {
          text: 'Firstname',
          align: 'start',
          sortable: false,
          value: 'name',
        },
        { text: 'Lastname', value: 'Lastname' },
        { text: 'Address', value: 'Address' },
        { text: 'Email ', value: 'Email' },
        { text: 'Position', value: 'Position' },
        { text: 'Phone', value: 'Phone' },
        { text: 'Subject', value: 'Subject' },
        { text: 'Action', value: 'Action' },
      ],
      desserts: [
        {
          name: 'Jhone',
          Lastname: 'Don',
          Address: 'London',
          Email: 'LONDON@gmail.com',
          Position: 'Teacher',
          Phone: '02054116414',
          Subject: 'English',
        },
        {
          name: 'Matherw',
          Lastname: 'KIN',
          Address: 'London',
          Email: 'LONDON@gmail.com',
          Position: 'Teacher',
          Phone: '02054116414',
          Subject: 'Mathematics',
        },
        {
          name: 'Jennifer',
          Lastname: 'KING',
          Email: 'LONDON@gmail.com',
          Address: 'London',
          Position: 'Teacher',
          Phone: '02054116414',
          Subject: 'History',
        },
        {
          name: 'Kven',
          Lastname: 'Json',
          Email: 'LONDON@gmail.com',
          Address: 'London',
          Position: 'Teacher',
          Phone: '02054116414',
          Subject: 'Geograpy',
        },
        {
          name: 'Gingerbread',
          Lastname: 'XING',
          Email: 'LONDON@gmail.com',
          Address: 'London',
          Position: 'Teacher',
          Phone: '02054116414',
          Subject: 'Lao',
        },
        {
          name: 'Jelly',
          Lastname: 'BAM',
          Email: 'LONDON@gmail.com',
          Address: 'London',
          Position: 'Teacher',
          Phone: '02054116414',
          Subject: 'Chemetry',
        },
        {
          name: 'Lollipop',
          Lastname: 'BONG',
          Email: 'LONDON@gmail.com',
          Address: 'London',
          Position: 'Teacher',
          Phone: '02054116414',
          Subject: 'Pysical',
        },
        {
          name: 'Bamm',
          Lastname: 'XING',
          Email: 'LONDON@gmail.com',
          Address: 'London',
          Position: 'Teacher',
          Phone: '02054116414',
          Subject: 'English',
        },
        {
          name: 'Mark',
          Lastname: 'XONG',
          Email: 'LONDON@gmail.com',
          Address: 'London',
          Position: 'Teacher',
          Phone: '02054116414',
          Subject: 'Lao',
        },
        {
          name: 'KitKat',
          Lastname: 'KONG',
          Email: 'LONDON@gmail.com',
          Address: 'London',
          Position: 'Teacher',
          Phone: '02054116414',
          Subject: 'Lao',
        },
      ],
    }
  },
}
</script>
