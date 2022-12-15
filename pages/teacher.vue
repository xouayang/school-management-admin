<template>
  <div class="mt-5">
    <v-row>
      <v-col cols="12" md="4" sm="12">
      <div class="text-h6 blue--text mb-8 font-weight-bold">Teachers</div>
      </v-col>
      <v-spacer />
     <v-col  cols="12" md="4" sm="12">
       <v-text-field outlined rounded dense label="Search">
        <template #append>
          <v-btn icon small>
            <v-icon class="pa-1">mdi-magnify</v-icon>
          </v-btn>
        </template>
      </v-text-field>
     </v-col>
      <v-col cols="12" md="4" sm="12" class="d-flex justify-end">
        <v-btn  color="primary" rounded @click="dialog = !dialog">
        <v-icon class="pr-3">mdi-plus-outline</v-icon>
        New Teacher
      </v-btn>
      </v-col>
    </v-row>
    <v-row>
      <v-col v-for="data in items" :key="data.id" cols="12" md="3" sm="12">
        <v-card class="rounded-xl flex" elevation="5">
          <div class="ms-4">
            <v-tooltip top color="primary">
              <template #activator="{ on, attrs }">
                <v-btn
                  icon
                  color="primary"
                  class="mt-1"
                  v-bind="attrs"
                  v-on="on"
                  to="/teacherDetails"
                >
                  <v-icon>mdi-dots-horizontal</v-icon>
                </v-btn>
              </template>
              <span>More Details</span>
            </v-tooltip>
          </div>
          <div class="d-flex flex-column align-center pt-3">
            <div>
              <v-avatar class="text-center" size="100">
                <v-img :src="data.image" alt="jhon" />
              </v-avatar>
            </div>
            <v-card-title class="indigo--text">{{ data.name }}</v-card-title>
            <v-card-text class="text-center">{{ data.subject }}</v-card-text>
            <div class="mb-6">
              <v-btn fab small color="primary" class="mr-6">
                <v-icon>mdi-email-outline</v-icon>
              </v-btn>
              <v-btn fab small color="primary">
                <v-icon>mdi-phone-outline</v-icon>
              </v-btn>
            </div>
          </div>
        </v-card>
      </v-col>
    </v-row>

    <!-- Dialog box Create Teacher -->
    <v-dialog v-model="dialog" persistent overlay-opacity="0.5" max-width="540">
      <v-card class="pb-4">
        <v-toolbar dark color="primary">
          <v-btn icon dark @click="dialog = !dialog">
            <v-icon>mdi-close</v-icon>
          </v-btn>
          <v-toolbar-title>Create Teacher </v-toolbar-title>
          <v-spacer></v-spacer>
          <v-toolbar-items>
            <v-btn text @click="dialog = !dialog"> Save </v-btn>
          </v-toolbar-items>
        </v-toolbar>
        <v-card class="mx-auto" max-width="800" elevation="0">
          <v-card-text>
            <div class="blue--text text-h5 mb-2">Create Teacher</div>
            <v-row>
              <v-col cols="12" sm="12">
                <v-text-field
                  label="Firstname"
                  dense
                  outlined
                  hide-details="auto"
                  append-icon="mdi-account-outline"
                />
              </v-col>
              <v-col cols="12" sm="12">
                <v-text-field
                  label="Lastname"
                  dense
                  outlined
                  hide-details="auto"
                  append-icon="mdi-account-outline"
                />
              </v-col>
              <v-col cols="12" sm="12">
                <v-text-field
                  label="Address"
                  dense
                  outlined
                  hide-details="auto"
                  append-icon="mdi-map-marker-outline"
                />
              </v-col>
              <v-col cols="12" sm="12">
                <v-text-field
                  label="Email"
                  type="email"
                  dense
                  outlined
                  hide-details="auto"
                  append-icon="mdi-email-outline"
                />
              </v-col>
              <v-col cols="12" sm="12">
                <v-text-field
                  label="Postion"
                  dense
                  outlined
                  hide-details="auto"
                  append-icon="mdi-account-details"
                >
                </v-text-field>
              </v-col>
              <v-col cols="12" sm="12">
                <v-text-field
                  label="Phone"
                  dense
                  outlined
                  hide-details="auto"
                  append-icon="mdi-phone"
                >
                </v-text-field>
              </v-col>
              <v-col cols="12" sm="12">
                <v-text-field
                  label="Subject"
                  dense
                  outlined
                  hide-details="auto"
                  append-icon="mdi-ab-testing"
                >
                </v-text-field>
              </v-col>
            </v-row>
          </v-card-text>
        </v-card>
      </v-card>
    </v-dialog>
  </div>
</template>
<script>
export default {
  name: 'TeacherPages',
  data() {
    return {
      dialog: false,
      items: [
        {
          id: 1,
          image: 'https://cdn.vuetifyjs.com/images/john.jpg',
          name: 'Jhon',
          subject: 'English',
        },
        {
          id: 2,
          image: 'https://cdn.vuetifyjs.com/images/john.jpg',
          name: 'Mathrew',
          subject: 'Mathematics',
        },
        {
          id: 3,
          image: 'https://cdn.vuetifyjs.com/images/john.jpg',
          name: 'Jennifer',
          subject: 'History',
        },
        {
          id: 4,
          image: 'https://cdn.vuetifyjs.com/images/john.jpg',
          name: 'Kven',
          subject: 'Geography',
        },
      ],
    }
  },
}
</script>