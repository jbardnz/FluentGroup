<template>
  <!-- Using Bootstrap grid system, split the webpage in 2 rows with 12 columns -->
  <div id="app" class="container">
    <div class="row header-row">
      <div class="col-md-6 center height">
        <Header />
      </div>
      <div class="col-md-6 center height">
        <AmountTable />
      </div>
    </div>
    <div class="row content-row">
      <div class="col-md-6 center">
        <Tab />
      </div>
      <div class="col-md-6 center">
        <History title="History" />
      </div>
    </div>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Tab from "./components/Tab";
import History from "./components/History";
import AmountTable from "./components/AmountTable";

export default {
  name: "App",
  components: {
    Header,
    AmountTable,
    Tab,
    History
  }
};
</script>

<style>
body {
  border-top: 10px solid green;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
.center {
  display: flex;
  justify-content: center;
  align-items: center;
}
.header-row {
  margin-top: 40px;
}
.content-row {
  margin-top: 70px;
  height: 100vh;
}
.height {
  height: 200px;
}
</style>
