<template>
  <v-app>
    <v-container align-center>
     <div>
       <h1>Blood Pressure</h1>
        <v-card>
          <SomeInfoChart ref="refChart" :title="myTitle" />
        </v-card>
      </div>
    </v-container>
  </v-app>
</template>

<script>
import SomeInfoChart from './components/SomeInfoChart'

export default {
  name: 'App',
  components: {
    SomeInfoChart
  },
  data () {
    return {
      myTitle: "Blood pressure"
    }
  },
}
</script>

<style lang="css" scoped>
div {
  text-align: center;
}

h1 {
  padding: 1rem;
}
</style>

