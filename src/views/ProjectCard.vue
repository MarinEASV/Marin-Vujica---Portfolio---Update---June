<template>
  <div>
    <!-- Conditional rendering based on project ID -->
    <div v-if="project.id === 1" class="project-card-one">
      <div class="project-content-one">
        <h3 class="project-title-one">{{ project.title }}</h3>
        <p class="project-description-one">{{ project.description }}</p>
        <a :href="project.linkUrl" class="project-link-one">LOOK THE WEBSITE</a> <!-- Added button -->
      </div>
      <img :src="project.imageUrl" :alt="project.title" class="project-image-one" />
    </div>

    <div v-else class="project-card">
      <div class="project-content">
        <h3 class="project-title">{{ project.title }}</h3>
        <p class="project-description">{{ project.description }}</p>
      </div>
      <img :src="project.imageUrl" :alt="project.title" class="project-image" />
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProjectCard',
  props: {
    project: Object
  }
};
</script>

<style scoped>
.project-card {
  display: flex;
  align-items: center;
  background-color: #384b47;
  padding: 20px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  max-width: 1000px;
  margin: 20px 0;
}

.project-content {
  flex: 1;
  padding-right: 20px;
}

.project-title {
  font-size: 1.5rem;
  color: #d3e8d7;
  margin-bottom: 10px;
}

.project-description {
  color: #d3e8d7;
}

.project-image {
  width: 300px;
  border-radius: 10px;
  object-fit: cover;
}

.project-card-one {
  background-color: #384b47;
  padding: 20px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  max-width: 800px;
  margin: 20px 0;
  text-align: left;
}

.project-content-one {
  padding-bottom: 20px;
}

.project-title-one {
  font-size: 1.5rem;
  color: #d3e8d7;
  margin-bottom: 10px;
}

.project-description-one {
  color: #d3e8d7;
}

.project-image-one {
  width: 100%;
  height: auto;
  object-fit: cover;
}

.project-link-one {
  display: inline-block;
  margin-top: 10px;
  padding: 10px 20px;
  background-color: #d3e8d7;
  color: #384b47;
  text-decoration: none;
  transition: background-color 0.5s;
}

.project-link-one:hover {
  background-color: #384b47;
  color: #d3e8d7;
  border-color: #d3e8d7;
  border-style: solid;
}
</style>
