<template>
  <v-container id="home" class="my-0 text-center home-container">
    <v-img
      src="@/assets/images/1.jpg"
      class="circular-image"
    />
    <p class="name-text">Louis Rafael E. Quiñones</p>
    <p class="title-text">Aspiring Programmer</p>
    <v-btn color="primary" class="mt-4" elevation="5" @click="viewWork">
      View My Work
    </v-btn>
  </v-container>
</template>

<script>
export default {
  name: 'HomePage',
  methods: {
    viewWork() {
      const element = document.getElementById('projects');
      if (element) {
        element.scrollIntoView({ behavior: 'smooth' });
      }
    },
  },
};
</script>

<style>
.home-container {
  background-image: url('@/assets/images/background.jpg');
  background-size: cover;
  background-position: center;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 20px;
  color: white;
  backdrop-filter: blur(10px); /* Glassmorphism */
}

.circular-image {
  width: 180px;
  height: 180px;
  border-radius: 50%;
  border: 4px solid rgba(255, 255, 255, 0.6);
  transition: transform 0.4s ease;
}

.circular-image:hover {
  transform: scale(1.1); /* Hover animation */
}

.name-text {
  font-size: 48px;
  font-weight: 700;
  margin-top: 10px;
  letter-spacing: 1px;
  font-family: 'Poppins', sans-serif;
}

.title-text {
  font-size: 20px;
  margin-top: 5px;
  font-style: italic;
}

.v-btn {
  background-color: #007bff;
  font-size: 18px;
  font-weight: 600;
  letter-spacing: 0.5px;
  transition: background-color 0.3s;
}

.v-btn:hover {
  background-color: #0056b3;
}
</style>
