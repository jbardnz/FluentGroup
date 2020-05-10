<template>
  <section>
    <div class="card-bg">
      <div class="card">
        <header class="card-header">
          <p class="card-header-title is-size-4">{{ title }}</p>
        </header>
        <div class="card-content">
          <div class="date-content">
            <p class="date">Due: Mon 12/02/19</p>
            <p class="earn">earn 50,000pts</p>
          </div>
          <div class="content is-bold">
            <p class="notes">Add Notes</p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus
            nec iaculis mauris.
          </div>
        </div>
        <footer class="card-footer">
          <a href="#" class="card-footer-item">Add your notes ></a>
        </footer>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: "Content",
  props: {
    title: String,
  },
};
</script>
<style scoped>
.date,
.earn,
.card-footer-item,
section {
  display: inline-block;
}
.card-content {
  padding: 0px;
}
.date-content {
  background-color: #1c355e;
  color: white;
  padding: 15px;
  font-weight: bold;
}
.content {
  padding: 15px;
}
.card-bg {
  display: inline-block;
  background-color: #f7f8fa;
}
.earn {
  float: right;
}
a {
  color: #42b983;
}
.card-footer-item {
  color: green;
  font-weight: bold;
}
</style>
