<template>
  <section class="is-large">
    <div class="content-section">
      <b-tabs type="is-boxed" v-model="activeTab">
        <b-tab-item label="Activity" icon="google-analytics" class="is-primary">
          <Content title="Next Step" />
        </b-tab-item>

        <b-tab-item label="Details" icon="check" disabled></b-tab-item>
      </b-tabs>
    </div>
  </section>
</template>

<script>
import Content from "./Content";

export default {
  data() {
    return {
      activeTab: 0
    };
  },
  name: "Tab",
  components: {
    Content
  },
  props: {
    title: String
  }
};
</script>

<style scoped>
.content-section {
  display: flex;
  justify-content: center !important;
  align-content: center !important;
}

.tab-item {
  width: 80%;
  box-shadow: 10px 10px 5px #8080806e;
}
.tabs li.is-active a {
  color: green !important;
}
.tabs li.is-active a > span {
  color: green;
}
</style>
