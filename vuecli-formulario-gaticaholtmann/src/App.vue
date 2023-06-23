<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <div class="container-challenge">
    <FormVue
    @add-info="addDates"
    ></FormVue>
  <TableView :datesList="dates">
  </TableView>
  </div>
</template>

<script>
import FormVue from './components/FormVue.vue'
import TableView from './components/TableView.vue';

export default {
  name: 'App',
  components: {
    FormVue,
    TableView
  },
  data() {
    return {
      dates:[]
    }
  },
  methods:{
    addDates(newDate){
      this.dates.push(newDate)
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.container-challenge{
  display: flex;
  justify-content: center;
}
</style>
