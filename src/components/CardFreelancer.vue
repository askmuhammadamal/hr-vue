<template>
  <div class="card shadow card-freelancer">
    <img :src="result.picture.large" class="card-img-top" alt="..." />
    <div class="card-body">
      <h5 class="card-title">{{ result.name.first }} {{ result.name.last }}</h5>
      <p class="card-text">
        <b-icon-telephone></b-icon-telephone> : {{ result.phone }} <br />
        <b-icon-envelope></b-icon-envelope> : {{ result.email }} <br />
        <b-icon-map></b-icon-map> : {{ result.location.country }} <br />
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardFreelancer",
  props: ["result"],
};
</script>

<style>
</style>