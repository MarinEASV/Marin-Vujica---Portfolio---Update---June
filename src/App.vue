<template>
  <div id="app">
    <Navbar />
    <header>
      <section class="hero-section mb-1">
      <div class="left-hero  bg-light-gray p-1">
                <h2 class="hello fs-secondary-heading fw-semi-bold text-black">Hello, I'm</h2>
            <div class="hero-bottom">
                <h1 class="fs-primary-heading text-black">MARIN VUJICA</h1>
                <h2 class="fs-secondary-heading  text-black">Freelance Graphic Designer</h2>
            </div>
        </div>
        <div class="right-hero ">
            <img src="/src/assets/Profile picture Marin.jpg" alt="multimedia and marketing related vector illustration pictograms">
        </div>
      </section>
    </header>
    <ProjectSection />
    <PhotographySection />
    <FlyerSection />
    <AppSection />
    <About />
    <Footer />
  </div>
</template>

<script>
import Navbar from './views/NavbarView.vue';
import ProjectSection from './views/ProjectSection.vue';
import PhotographySection from './views/PhotographySection.vue';
import FlyerSection from './views/FlyerSection.vue';
import AppSection from './views/AppSection.vue';
import About from './views/AboutView.vue';
import Footer from './views/FooterView.vue';

export default {
  name: 'App',
  components: {
    Navbar,
    ProjectSection,
    PhotographySection,
    FlyerSection,
    AppSection,
    About,
    Footer
  }
};
</script>

<style scoped>
.hero-section{
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1.5em;
  min-height: 85vh;
  background-color: #d3e8d7;
}

.left-hero {
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 1em;
}



.right-hero {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 1em;
}

.right-hero img{
  max-width: 50%;
  height: auto;
  object-fit: cover;
}


@media (max-width: 1000px){
  .hero-section{
    display: flex;
    flex-direction: column;
    height: auto;
    gap: 1.5em;
  }
  
  .left-hero{
    width: 100%;
    height: auto;
  }

  .hello{
    margin-bottom: 2.5em;}

  .right-hero{
    margin: 0 auto;
    height: auto;
    width: 100%;
  }
}

@media (max-width: 768px){
 /* Hero Section */
 .hero-section{
    display: flex;
    flex-direction: column;
    gap: 1.5em;
    height: auto;
  }

  .left-hero{
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }

  .hello{
    margin-bottom: 2.5em;
  }

  .right-hero{
    display: flex;
  }  
}
</style>
