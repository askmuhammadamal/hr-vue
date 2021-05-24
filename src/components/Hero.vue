<template>
  <div class="container mt-4">
    <!-- Desktop -->
    <div class="d-md-block d-none">
      <div class="row">
        <div class="col-md-6">
          <div class="d-flex h-100">
            <div class="justify-content-center align-self-center">
              <h2><strong>Human Resources</strong><br />in your pocket.</h2>
              <p>Hire the best freelancers for any job, online.</p>
              <router-link to="/freelancers" class="btn btn-lg btn-info"
                >Hire a Freelancer</router-link
              >
            </div>
          </div>
        </div>
        <div class="col-md-6">
          <img src="../assets/images/illustration.svg" width="100%" />
        </div>
      </div>
    </div>

    <!-- Mobile -->
    <div class="d-sm-block d-md-none">
      <div class="row">
        <div class="col-md-6">
          <img src="../assets/images/illustration.svg" width="100%" />
        </div>
        <div class="col-md-6 mt-4">
          <div class="d-flex h-100">
            <div class="justify-content-center align-self-center">
              <h2><strong>Human Resource</strong><br />in your pocket.</h2>
              <p>Hire the best freelancers for any job, online.</p>
              <router-link to="/freelancers" class="btn btn-lg btn-info"
                >Hire a Freelancer</router-link
              >
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Hero",
};
</script>

<style>
</style>