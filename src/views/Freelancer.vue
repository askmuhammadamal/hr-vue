<template>
  <div>
    <Navbar />
    <div class="container">
      <div class="col mt-5">
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
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from "@/components/Navbar.vue";
import CardFreelancer from "@/components/CardFreelancer.vue";
import axios from "axios";

export default {
  name: "Freelancer",
  components: {
    Navbar,
    CardFreelancer,
  },
  data() {
    return {
      results: [],
      quantity: 20,
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

<style>
</style>