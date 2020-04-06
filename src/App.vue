<template>
  <div>
    <div id="slogan" class="text-center">
      <h1>Name Generator</h1>
      <br />
      <h6 class="text-secundary">Name generator using Vue.js, GraphQL and Node.js</h6>
    </div>
    <div id="main">
      <div class="container">
        <div class="row">
          <div class="col-md">
            <h5>
              Prefixes
              <span class="badge badge-info">5</span>
            </h5>
            <div class="card">
              <div class="card-body">
                <ul class="list-group">
                  <li
                    class="list-group-item"
                    v-for="prefix in prefixes"
                    v-bind:key="prefix"
                  >{{prefix}}</li>
                  <br />
                  <input type="text" class="form-control" placeholder="Tape prefix" />
                </ul>
              </div>
            </div>
          </div>
          <div class="col-md">
            <h5>
              Suffixes
              <span class="badge badge-info">5</span>
            </h5>
            <div class="card">
              <div class="card-body">
                <ul class="list-group">
                  <li
                    class="list-group-item"
                    v-for="suffix in suffixes"
                    v-bind:key="suffix"
                  >{{suffix}}</li>
                  <br />
                  <input type="text" class="form-control" placeholder="Tape suffix" />
                </ul>
              </div>
            </div>
          </div>
        </div>
        <br />
        <h5>
          Domains
          <span class="badge badge-info">5</span>
        </h5>
        <div class="card">
          <div class="card-body">
            <ul class="list-group">
              <li class="list-group-item" v-for="domain in domains" v-bind:key="domain">
                {{domain}}
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import "bootstrap/dist/css/bootstrap.css";
import "font-awesome/css/font-awesome.css";

export default {
  name: "app",
  data: function() {
    return {
      prefixes: ["Air", "Jet", "Flight"],
      suffixes: ["Hub", "Station", "Mart"],
      domains: [
        "AirHub",
        "AirStation",
        "AirMart",
        "JetHub",
        "JetStation",
        "JetMart",
        "FlightHub",
        "FlighStation",
        "FlightMart"
      ]
    };
  }
};
</script>

<style>
#slogan {
  margin-top: 30px;
  margin-bottom: 30px;
}

#main {
  background-color: #f1f1f1;
  padding-top: 30px;
  padding-bottom: 30px;
}
</style>
