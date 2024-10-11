<template>
  <v-container id="projects" class="my-5">
    <h1 class="white--text">Projects</h1>
    <v-row>
      <v-col v-for="project in projects" :key="project.title" cols="12" md="6" lg="4">
        <v-card class="project-card mb-3" elevation="2">
          <v-card-title>
            <a :href="project.link" target="_blank" rel="noopener noreferrer" class="white--text">
              {{ project.title }}
            </a>
          </v-card-title>
          <v-card-text class="white--text">{{ project.description }}</v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'ProjectsPage',
  data() {
    return {
      projects: [
        {
          title: 'Project One',
          description: 'Description of project one.',
          link: 'https://github.com/yourusername/project-one',
        },
        {
          title: 'Project Two',
          description: 'Description of project two.',
          link: 'https://github.com/yourusername/project-two',
        },
        // Add more projects as needed
      ],
    };
  },
};
</script>

<style scoped>
.white--text {
  color: white;
}

.project-card {
  transition: transform 0.3s ease, background-color 0.3s ease; /* Smooth transition for hover effects */
  background-color: rgba(60, 45, 30, 0.8); /* Background color with slight transparency */
  border-radius: 8px; /* Adds rounded corners to the card */
}

.project-card:hover {
  transform: scale(1.05); /* Slightly enlarges the card on hover */
  background-color: rgba(70, 55, 40, 0.9); /* Darker shade on hover */
}
</style>
