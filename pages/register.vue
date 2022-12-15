<template>
  <div class="mt-10">
    <v-row class="pa-3">
      <v-card class="mx-auto" width="460" elevation="5" rounded="lg">
        <div class="text-center mt-2">
          <v-btn fab x-large color="success"
            ><v-icon>mdi-login-variant</v-icon></v-btn
          >
        </div>
        <div class="font-weight-bold text-center mt-3">Sign Up</div>
        <v-col cols="12">
          <v-text-field
            outlined
            dense
            hide-details="auto"
            label="Username"
            placeholder="example: Jhone"
            append-icon="mdi-account-outline"
          />
        </v-col>
        <v-col cols="12">
          <v-text-field
            outlined
            dense
            hide-details="auto"
            label="Telephone"
            placeholder="example:02054116077"
            append-icon="mdi-phone-outline"
          />
        </v-col>
        <v-col cols="12">
          <v-autocomplete
            ref="country"
            :items="countries"
            label="User_Type"
            placeholder="Select..."
            outlined
            dense
            hide-details="auto"
            required
          ></v-autocomplete>
        </v-col>
        <v-col cols="12">
          <v-text-field
            outlined
            dense
            label="Password"
            hide-details="auto"
            :type="hidePassword ? 'text' : 'password'"
          >
            <template #append>
              <v-btn
                icon
                color="primary"
                small
                @click="hidePassword = !hidePassword"
                ><v-icon class="pb-2">{{
                  hidePassword ? 'mdi-eye-outline' : 'mdi-eye-off'
                }}</v-icon></v-btn
              >
            </template>
          </v-text-field>
        </v-col>
        <v-col cols="12" class="mb-6">
            <v-btn block color="primary" style="text-transform: inherit">Sign Up</v-btn>
        </v-col>
      </v-card>
    </v-row>
  </div>
</template>
<script>
export default {
  name: 'RegisterPages',
  layout: 'blank',
  data() {
    return {
      hidePassword: false,
      countries: ['Teacher', 'Student'],
    }
  },
}
</script>