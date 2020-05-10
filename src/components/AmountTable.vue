 <template>
  <section>
    <div class="card">
      <header class="card-header">
        <p class="card-header-title">Due Date</p>
      </header>

      <div class="card-content">
        <div class="date-content">
          <h1 class="date">12/02/20</h1>
        </div>
      </div>
    </div>
    <div class="card">
      <header class="card-header">
        <p class="card-header-title">Amount(USD)</p>
      </header>

      <div class="card-content">
        <div class="amount-content">
          <h1 class="amount">$250,000.00</h1>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AmountTable",
  props: {
    title: String
  }
};
</script>

<style scoped>
.card {
  display: inline-block;
  margin-right: 20px;
  border-radius: 5px;
  width: 150px;
}
.card-header {
  background-color: #00800024;
}
.card-header > p {
  justify-content: center;
}
.card-content {
  text-align: center;
}
.card:hover {
  box-shadow: 5px 5px 5px 5px#8080806e;
}
</style>