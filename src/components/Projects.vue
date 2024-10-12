<template>
  <v-container id="projects" class="my-5">
    <h1 class="white--text">Projects</h1>
    <v-row>
      <v-col v-for="project in projects" :key="project.title" cols="12" md="6" lg="4">
        <v-card class="project-card mb-3" elevation="2">
          <v-img :src="project.image" height="200px" class="project-image" />
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
          title: 'To-Do List',
          description: 'This To-Do List application is a simple yet powerful tool for managing daily tasks efficiently. Built using modern web technologies, it allows users to add, update, and delete tasks in an intuitive interface. The application features task prioritization, due date management, and filtering options to help users stay organized and productive. With its sleek, responsive design, it ensures a seamless experience on both desktop and mobile devices. Whether for personal use or team collaboration, this app offers a user-friendly way to keep track of tasks and deadlines.',
          link: 'https://louis-rafael-vue.vercel.app/',
          image: require('@/assets/images/todolist.png'), // Add image for the project
        },
        {
          title: 'Project Two',
          description: 'Description of project two.',
          link: 'https://github.com/yourusername/project-two',
          image: require('@/assets/images/profile.jpg'), // Another project image
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
  transition: transform 0.3s ease, background-color 0.3s ease;
  background-color: rgba(60, 45, 30, 0.8);
  border-radius: 8px;
}

.project-card:hover {
  transform: scale(1.05);
  background-color: rgba(70, 55, 40, 0.9);
}

.project-image {
  border-radius: 8px 8px 0 0; /* Rounded top corners to match the card */
}
</style>
