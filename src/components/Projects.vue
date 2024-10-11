<template>
    <v-container id="projects" class="my-5">
      <h1 class="white--text">Projects</h1>
      <v-row>
        <v-col v-for="project in projects" :key="project.title" cols="12" md="6" lg="4">
          <v-card class="mb-3" elevation="2">
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
  
  <style>
  .white--text {
    color: white;
  }
  </style>
  