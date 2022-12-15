<template>
  <div class="mt-15">
    <v-row>
    <v-col cols="12" md="6" sm="12" class="mx-auto">
       <v-card class="mx-auto rounded-lg" width="500">
        <v-card-title class="text-center">SignIn</v-card-title>
        <v-card-text
          >Doesn't have an account ?
          <v-btn text class="blue--text font-weight-bold" style="text-transform: lowercase" to="/register">Sign Up</v-btn>
        </v-card-text>
        <v-col cols="12" md="12" sm="12">
          <v-text-field
            outlined
            dense
            hide-details="auto"
            placeholder="example : Jhone"
            label="Username"
            append-icon="mdi-account-outline"
          />
        </v-col>
        <v-col cols="12" md="12" sm="12">
          <v-text-field
            outlined
            dense
            label="Password"
            placeholder="Enter 6 charater or more"
            hide-details="auto"
            :type="hidePassword ? 'text' : 'password'"
          >
            <template #append>
              <v-btn icon @click="hidePassword = !hidePassword"
                ><v-icon color="primary" class="pb-2">{{
                  hidePassword ? ' mdi-eye-outline' : 'mdi-eye-off-outline'
                }}</v-icon></v-btn
              >
            </template>
          </v-text-field>
          <v-spacer />
          <div class="d-flex justify-end mt-1">
            <div class="blue--text font-weight" style="cursor: pointer">
              forgot password
            </div>
          </div>
        </v-col>
        <v-col cols="12" sm="12">
          <v-btn block color="primary" style="text-transform: inherit">Sign In</v-btn>
        </v-col>
      </v-card>
    </v-col>
    </v-row>
  </div>
</template>
<script>
export default {
  name: 'LoginPages',
  layout: 'blank',
  data() {
    return {
      hidePassword: false,
    }
  },
}
</script>