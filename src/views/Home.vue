<template>
  <div class="home">
    <Navbar />
    <div class="container">
      <Hero />

      <div class="row mt-4">
        <div class="col-lg-6">
          <h2>Freelancer <strong>Star</strong></h2>
        </div>
        <div class="col-lg-6">
          <router-link to="/freelancers" class="btn btn-info float-right"
            ><b-icon-eye></b-icon-eye> View All</router-link
          >
        </div>
      </div>

      <div class="row mb-4">
        <div
          class="col-md-4 mt-4"
          v-for="result in results"
          :key="result.id.value"
        >
          <CardFreelancer :result="result" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from "@/components/Navbar.vue";
import Hero from "@/components/Hero.vue";
import CardFreelancer from "@/components/CardFreelancer.vue";
import axios from "axios";

export default {
  name: "Home",
  components: {
    Navbar,
    Hero,
    CardFreelancer,
  },
  data() {
    return {
      results: [],
      quantity: 3,
    };
  },
  methods: {
    setfreelancers(data) {
      this.results = data.results;
    },
  },
  mounted() {
    axios
      .get("https://randomuser.me/api/?results=" + this.quantity)
      .then((response) => this.setfreelancers(response.data))
      .catch((error) => console.log(error));
  },
};
</script>
