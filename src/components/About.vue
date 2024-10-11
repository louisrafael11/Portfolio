<template>
  <v-container id="about" class="my-5 text-center">
    <h1 class="white--text">About Me</h1>
    <p class="white--text">
      I am Louis Rafael E. Quiñones, a third-year Information Technology student at Caraga State University.
    </p>
  </v-container>
</template>

<script>
export default {
  name: 'AboutPage',
};
</script>

<style>
.white--text {
  color: white;
}

.circular-image {
  width: 150px; /* Set the desired width */
  height: 150px; /* Set the desired height */
  border-radius: 50%; /* Makes the image circular */
  margin: 20px auto; /* Center the image */
}
</style>
