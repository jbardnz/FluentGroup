<template>
  <div class="header">
    <div class="accredited-sales">
      <div class="go-back">
        <b-icon icon="chevron-left" size="is-small" type="is-success"></b-icon>
        <a>Go Back</a>
      </div>
      <p class="in-progess">In progress</p>
      <h1 class="header-text">The Accredited Sales Executive (ASE) End-point app</h1>
      <button class="update-button">Add Update</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",
  props: {
    title: String
  }
};
</script>

<style scoped>
.accredited-sales {
  display: inline-block;
}

.in-progess {
  display: inline-block;
  padding: 2px 5px;
  border: 1px solid green;
  border-radius: 10px;
  background-color: #00800024;
  color: green;
  font-size: 13px;
  font-weight: bold;
  margin-bottom: 20px;
}

.header-text {
  font-size: 25px;
  font-weight: bold;
  margin-bottom: 20px;
}

.update-button {
  background-color: green;
  color: white;
  padding: 10px;
  border-radius: 8px;
}
.go-back {
  position: absolute;
  top: -16px;
  width: 85px;
  height: auto;
}
.go-back > a:hover {
  color: green;
}

/* using Media Queries for responsive design  */
@media screen and (max-width: 600px) {
  .header-text {
    font-size: 22px;
  }
  .update-button {
    font-size: 13px;
  }
  .in-progess {
    font-size: 10px;
  }
  .content-row {
    margin-top: 25px;
  }
}
</style>
