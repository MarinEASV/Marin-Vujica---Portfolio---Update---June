  <template>
    <section id="projects">
      <h2 class="h2-projects">MY RECENT PROJECTS</h2>
      <div class="projects-container">
        <ProjectCard v-for="project in projects" :key="project.id" :project="project" />
      </div>
    </section>
  </template>

  <script>
  import ProjectCard from './ProjectCard.vue';
  import trapholtImage from '/src/assets/trapholt.jpg';
  import nannaImage from '/src/assets/_MiniMI.jpg';

  export default {
    name: 'ProjectSection',
    components: {
      ProjectCard
    },
    data() {
      return {
        projects: [
          {
            id: 1,
            title: 'TRAPHOLT MUSEUM',
            description: 'Our team of 4 took on a project to develop a comprehensive visual identity and website for Trapholt Museum in Kolding, with a specific focus on targeting a particular group of people. We began by doing research to understand the preferences and interests of our target audience. Using this information as a guide, we collaborated closely to create a cohesive visual identity with elements such as a logo, color palette, typography, and overall design style made to resonate with our chosen demographic.',
            imageUrl: trapholtImage,
            linkUrl: 'https://jakubrepa.github.io/index.html'             

          },
          {
            id: 2,
            title: 'ILLUSTRATION',
            description: 'As part of a study assignment to practice using Adobe Illustrator, I had a fun project to create a creative, imaginary illustration of myself. I started by learning the basics of Illustrator, like how to draw shapes, use colors, and add details. It was exciting to see how I could bring my ideas to life on the computer screen, and the process helped me improve my skills in digital art and illustration. This project not only allowed me to express my creativity but also gave me valuable experience using Illustrator for future design projects.',
            imageUrl: nannaImage
          },
        ]
      };
    }
  };
  </script>

  <style scoped>
  #projects {
    padding: 40px 20px;
    background-color: #d3e8d7;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .h2-projects {
    font-size:100px;
    
  }
  .projects-container {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 20px;
  }
  </style>
