<template>
    <div class="mt-4">
       <v-row>
        <v-col cols="12" md="4" sm="12">
          <div class="blue--text text-h6 font-weight-bold">News</div>
        </v-col>
        <v-col cols="12" md="4" sm="12">
          <v-text-field label="Search" dense outlined rounded append-icon="mdi-magnify"/>
        </v-col>
        <v-col cols="12" md="4" sm="12" class="d-flex justify-end">
          <v-btn rounded color="primary" @click="dialog = !dialog">
            <v-icon class="me-3">mdi-plus-outline</v-icon>
            Post news
          </v-btn>
        </v-col>
       </v-row>
        <v-dialog v-model="dialog" persistent overlay-opacity="0.5" max-width="540">
      <v-card class="pb-4">
        <v-toolbar dark color="primary">
          <v-btn icon dark @click="dialog = !dialog">
            <v-icon>mdi-close</v-icon>
          </v-btn>
          <v-toolbar-title>Post news </v-toolbar-title>
          <v-spacer></v-spacer>
          <v-toolbar-items>
            <v-btn text @click="dialog = !dialog"> Save </v-btn>
          </v-toolbar-items>
        </v-toolbar>
        <v-card class="mx-auto" max-width="800" elevation="0">
          <v-card-text>
            <div class="blue--text text-h5 mb-4">Post News</div>
            <v-row>
              <v-col cols="12" sm="12">
                <v-text-field
                  label="Title"
                  dense
                  outlined
                  hide-details="auto"
                  append-icon="mdi-identifier"
                />
              </v-col>
              <v-col cols="12" sm="12">
                <v-text-field
                  label="Details"
                  dense
                  outlined
                  hide-details="auto"
                  append-icon="mdi-account-details-outline"
                />
              </v-col>
              <v-col cols="12" sm="12">
                <v-text-field
                  label="Images"
                  dense
                  outlined
                  hide-details="auto"
                  append-icon="mdi-account-group-outline"
                />
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
    name:'NewPages',
    data() {
      return {
        dialog : false
      }
    }
}
</script>