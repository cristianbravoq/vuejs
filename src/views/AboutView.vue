<template>
  <div class="about">
    <div class="container">
        <div class="section-content">
            <div class="text-center">
              <div class="btn-group my-4" role="group" aria-label="Basic mixed styles example">
                <button type="button" class="btn btn-danger"><router-link style="text-decoration: none; color: black;" to="/">Home</router-link></button>
                <button type="button" class="btn btn-success"><router-link style="text-decoration: none; color: black;" to="/about">Find flight route</router-link></button>
              </div>
                    <div class="alert alert-success" role="alert">
                        <div class="row text-center">
                            <p>Press Find flight route.</p>
                        </div>
                        <div class="alert alert-warning" role="alert">
                            You have not yet performed a search
                        </div>
                          <table class="table table-hover">
                              <thead>
                                <tr>
                                  <th scope="col">Origin</th>
                                  <th scope="col">Destination</th>
                                  <th scope="col">Price</th>
                                </tr>
                              </thead>
                              <tbody>
                                <tr>
                                  <th scope="row">Departure Station</th>
                                  <td>Arrival Station</td>
                                  <td>USD Price first stopover</td>
                                </tr>
                                <tr>
                                  <th scope="row">Departure Station</th>
                                  <td>Arrival Station</td>
                                  <td>USD Price second stopover</td>
                                </tr>
                                <tr>
                                  <th scope="row">Departure Station</th>
                                  <td>Arrival Station</td>
                                  <td>USD Price third stopover</td>
                                </tr>
                              </tbody>
                              <tbody>
                                  <tr>
                                    <td colspan="2">PRICE:
                                      <button type="button" class="btn btn-success">USD</button>
                                        <button type="button" class="btn btn-success">EUR</button>
                                        <button type="button" class="btn btn-success">GBP</button>
                                      </td>
                                    <td>Coin</td>
                                  </tr>
                              </tbody>
                          </table>
                    </div>
            </div>
        </div>
    </div>
  </div>
</template>
