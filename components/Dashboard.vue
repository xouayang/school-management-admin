<template>
  <div class="mt-6">
    <v-row>
      <v-col v-for="data in items" :key="data.id" cols="12" md="3" sm="12">
        <v-card class="pa-3 rounded-lg" elevation="5">
          <div class="d-flex">
            <v-btn fab  color="success">
               <v-icon>
               {{data.icon}}
              </v-icon>
            </v-btn>
            <v-spacer/>
             <div class="d-flex flex-column align-center">
              <span>{{data.title}}</span>
              <span class="text-center font-weight-bold text-h6">{{data.amout}}</span>
              </div>
          </div>
        </v-card>
      </v-col>
    </v-row>
  </div>
</template>
<script>
export default {
  name: 'DashboardPages',
  data() {
    return {
      items:[
        {
          id:1,
          icon:'mdi-account-group-outline',
         title:'Students',
         amout:400
        },
        {
          id:2,
           icon:'mdi-human-male-board',
          title:'Teachers',
          amout:500
        },
        {
          id:3,
           icon:'mdi-chart-timeline-variant-shimmer',
           title:'Activity',
           amout:200
        },
        {
          id:4,
           icon:'mdi-new-box',
           title:'News',
           amout:100
        }
      ]
    }
  }
}
</script>