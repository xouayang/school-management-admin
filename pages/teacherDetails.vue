<template>
  <div class="mt-3">
    <div class="d-flex">
      <div class="blue--text text-h6 font-weight-bold">
        Teacher Personal Information
      </div>
      <v-spacer />
    </div>
    <div class="mt-4">
      <v-row>
        <v-col cols="12" md="12" sm="12">
            <v-card class="rounded-xl" width="1000">
              <v-img
                height="200"
                src="https://cdn.pixabay.com/photo/2020/07/12/07/47/bee-5396362_1280.jpg"
              >
                <v-card-title class="white--text">
                  <v-avatar size="56" class="color-white">
                    <img
                      style="border: 2px solid white"
                      alt="user"
                      src="https://cdn.pixabay.com/photo/2020/06/24/19/12/cabbage-5337431_1280.jpg"
                    />
                  </v-avatar>
                  <div class="ml-3">Jennifer</div>
                </v-card-title>
              </v-img>
              <div class="pa-6">
                <v-row class="ms-15 mt-4">
                 <v-col cols="12" md="4" sm="12">
                   <div>Teacher</div>
                  <div>
                    <v-icon color="error">mdi-map-marker-outline</v-icon> Vientiane Capital
                  </div>
                 </v-col>
                 <v-col cols="12" md="4" sm="12">
                   <div>Phone</div>
                  <div><v-icon color="error" class="pe-2">mdi-phone-outline</v-icon>020XXXXXXXX</div>
                 </v-col>
                 <v-col cols="12" md="4" sm="12">
                   <div>Email</div>
                  <div>  <v-icon color="error" class="pe-2">mdi-email-outline</v-icon>XXXXXX@gmail.com</div>
                 </v-col>
                </v-row>
              </div>
            </v-card>
        </v-col>
      </v-row>
    </div>
  </div>
</template>
<script>
export default {
  name:'TeacherDetails',
  data() {
    return {
      hideInfomation:false
    }
  }
}
</script>