<template>
  <div class="about">
    <div class="container">
        <div class="section-content">
            <div class="text-center">
              <div class="btn-group my-4" role="group" aria-label="Basic mixed styles example">
                <button type="button" class="btn btn-success"><router-link style="text-decoration: none; color: black;" to="/">Home</router-link></button>
              </div>
                    <div class="alert alert-success" role="alert">
                      <p style="text-transform: uppercase;">Enter the city of origin and destination city to save the route</p>
                        <div class="form-group d-flex" style="border: 2px solid; padding: 2em">
                          <label for="" style="margin: 5px">Departure Station</label>
                          <input type="text" class="form-control" v-model="registro.departureStation"> 
                          <label for="" style="margin: 5px">Arrival Station</label>
                          <input type="text" class="form-control" v-model="registro.arrivalStation">
                          <button class="btn btn-success row" style="margin: 5px" @click="agregarRuta">SEND</button>
                        </div>
                        <hr>
                          <table class="table table-hover">
                              <thead>
                                <tr>
                                  <th scope="col">Origin</th>
                                  <th scope="col">Destination</th>
                                  <th scope="col"></th>
                                </tr>
                              </thead>
                              <tbody v-if="registros.length">
                                <tr v-for="(registro, index) in registros">
                                  <td>{{registro.departureStation}}</td>
                                  <td>{{registro.arrivalStation}}</td>
                                  <td><button @click="remove" class="btn btn-danger">Remove</button></td>
                                </tr>
                              </tbody>
                          </table>
                    </div>
            </div>
        </div>
    </div>
  </div>
</template>

<script>

  export default {
    titulo: '',
    name: 'app',
    data () {
      return {
        registro: {
          departureStation: '',
          arrivalStation: ''
        },
        registros : [ ]
      }
    },
    methods: {
      agregarRuta: function() {
        const { departureStation, arrivalStation } = this.registro;
        this.registros.push({
          departureStation,
          arrivalStation
        })
      },
      remove: function(index) {
        const { departureStation, arrivalStation } = this.registro;
        this.registros.splice(index, 1);
      }
    }
  }

</script>
