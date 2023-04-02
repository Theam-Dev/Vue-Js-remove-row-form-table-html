<template>
  <nav class="navbar navbar-expand-sm bg-dark navbar-dark">
    <div class="container">
      <a class="navbar-brand" href="#">Tutorial Sharing</a>
    </div>
  </nav>
  <div class="container mt-3">
    <table class="table">
      <thead>
        <tr>
          <th>Id</th>
          <th>Name</th>
          <th>Email</th>
          <th>Remove</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(item, index) in data" :key="index">
          <td>{{ item.id }}</td>
          <td>{{ item.name }}</td>
          <td>{{ item.email }}</td>
          <td>
            <button class="btn btn-primary btn-sm" v-on:click="removeRow(index)">remove</button>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>
<script>
import "bootstrap/dist/css/bootstrap.min.css";
export default {
  name: 'App',
  data() {
    return {
      data: [
        {"id": 1,"name": "Francis","email": "Marley.Hermiston64@hotmail.com"},
        {"id": 2,"name": "Jay","email": "Amanda.White56@gmail.com"},
        {"id": 3,"name": "Marianna","email": "Kiarra.DuBuque@gmail.com"},
        {"id": 4,"name": "Kamron","email": "Patience13@gmail.com"},
        {"id": 5,"name": "Antone","email": "Armando.Bauch@gmail.com"}
      ]
    }
  },
  methods:{
    removeRow(index){
      this.data.splice(index, 1);
    }
  }
}
</script>