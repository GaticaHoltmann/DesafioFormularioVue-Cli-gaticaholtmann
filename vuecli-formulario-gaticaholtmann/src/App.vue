<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <div class="container-challenge">
    <FormVue
    @clickButton="addDates"
    ></FormVue>
  <TableView>
    <tr v-for="(date, index) in dates" :key="index">
      <td>{{ date.name }}</td>
      <td>{{ date.email }}</td>
      <td>{{ date.date }}</td>
      <td>{{ date.area }}</td>
    </tr>
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
      currentData:{},
      dates:[
        {name: "david", date:"1/1/1", email:"a@cl.com", area:"prueba"}
      ]
    }
  },
  methods:{
    addDates(){
      
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
