<template>
  <v-container id="about" class="my-5 text-center">
    <h1 class="white--text">About Me</h1>
    <v-card class="about-card" elevation="5">
      <v-card-text>
        <p class="white--text">
          I am Louis Rafael E. Quiñones, a third-year Information Technology student at Caraga State University.
        </p>
      </v-card-text>
    </v-card>
  </v-container>
</template>

<script>
export default {
  name: 'AboutPage',
};
</script>

<style scoped>
.white--text {
  color: white;
}

.about-card {
  background-color: rgba(60, 45, 30, 0.8); /* Background color with slight transparency */
  border-radius: 8px;
  padding: 20px; /* Adds padding inside the card */
  margin-top: 20px; /* Adds space above the card */
  transition: transform 0.3s ease, background-color 0.3s ease; /* Smooth transition for hover effects */
}

.about-card:hover {
  transform: scale(1.05); /* Slightly enlarges the card on hover */
  background-color: rgba(70, 55, 40, 0.9); /* Darker shade on hover */
}

.circular-image {
  width: 150px; /* Set the desired width */
  height: 150px; /* Set the desired height */
  border-radius: 50%; /* Makes the image circular */
  margin: 20px auto; /* Center the image */
}
</style>
