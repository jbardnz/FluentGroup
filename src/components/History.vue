<template>
  <section>
    <div class="container">
      <h1 class="is-size-4 is-bold history-title">{{title}}</h1>
      <div class="timeline-item" date-is="Now"></div>

      <div class="timeline-item" date-is="Tue 5/02/2019">
        <h1>
          <b>Onsite meeting</b>
        </h1>
        <h2>
          <p>Attendees:</p>
          <span>Art Vandelay, Jackie Chiles</span>
        </h2>
        <h2>
          <p>Discussed:</p>
          <span>Current network infrastructure design and BigS focus areas for next FY. Proposed product test drive and/or SLR for next steps.</span>
        </h2>
      </div>

      <div class="timeline-item" date-is="Tue 6/02/2019">
        <h1>
          <b>Prospects added from Penske Inc.</b>
        </h1>
        <a>View prospects ></a>
      </div>
      <div class="timeline-item" date-is="Tue 7/02/2019">
        <h1>
          <b>HPE Activity approved</b>
        </h1>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "History",
  props: {
    title: String
  }
};
</script>



<style scoped>
.container {
  width: 75%;
  margin: 0 auto;
}
.history-title {
  font-weight: bold;
  margin-bottom: 25px;
}
.timeline-item {
  padding: 3em 2em 2em;
  position: relative;
  color: green;
  border-left: 2px solid green;
}
.timeline-item p {
  font-size: 1rem;
}
.timeline-item > a {
  color: green;
  font-weight: bold;
}
.timeline-item::before {
  content: attr(date-is);
  position: absolute;
  left: 2em;
  font-weight: bold;
  top: 1em;
  display: block;
  font-family: "Roboto", sans-serif;
  font-size: 0.785rem;
  color: black;
  opacity: 0.5;
}
.timeline-item::after {
  width: 15px;
  height: 15px;
  display: block;
  top: 1em;
  position: absolute;
  left: -8px;
  border-radius: 10px;
  content: "";
  border: 2px solid green;
  background: green;
}

.timeline-item > h1 {
  color: black;
  margin-bottom: 10px;
}
.timeline-item > h2 {
  color: black;
  margin-bottom: 10px;
}
.timeline-item > h2 > p {
  font-style: italic;
}

.timeline-item:last-child {
  -webkit-border-image: -webkit-gradient(
      linear,
      left top,
      left bottom,
      color-stop(60%, green),
      to(green)
    )
    1 100%;
  -webkit-border-image: linear-gradient(to bottom, green 60%, green) 1 100%;
  -o-border-image: linear-gradient(to bottom, green 60%, green) 1 100%;
  border-image: -webkit-gradient(
      linear,
      left top,
      left bottom,
      color-stop(60%, green),
      to (green)
    )
    1 100%;
  border-image: linear-gradient(to bottom, green 60%, green) 1 100%;
}

/* using Media Queries for responsive design  */
@media screen and (max-width: 600px) {
  .container {
    margin-top: 54px;
  }
}
</style>