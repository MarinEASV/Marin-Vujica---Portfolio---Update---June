<template>
  <div class="wrapper">
    <nav class="navbar bg-black">
      <a href="" class="logo-link"><img src="/src/assets/Logo PORTFOLIO.svg" alt="Marin Logo" class="logo" /></a>
        <ul :class="{ 'nav-menu': true, 'active': isMenuOpen }">
          <li class="nav-item"><a @click="toggleMenu" href="#projects" class="fs-nav nav-link">PROJECTS</a></li>
          <li class="nav-item"><a @click="toggleMenu" href="#about" class="fs-nav nav-link">ABOUT ME</a></li>
          <li class="nav-item"><a @click="toggleMenu" href="#contact" class="fs-nav nav-link">CONTACT</a></li>
          <li class="nav-item"><a href="https://www.youtube.com/watch?v=DnjCWJMrWko" target="_blank" class="fs-nav nav-link">VIDEO CV</a></li>
          <li class="nav-item"><a href="https://acrobat.adobe.com/id/urn:aaid:sc:EU:ab6f3c3d-ad90-4aa8-8169-452c0a258115" target="_blank" class="fs-nav nav-link">CV</a></li>
        </ul>
        <div class="hamburger" :class="{ 'active': isMenuOpen }" @click="toggleMenu">
          <span :class="{ 'bar': true, 'active': isMenuOpen }" v-for="n in 3" :key="n"></span>
        </div>
    </nav>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const isMenuOpen = ref(false);

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
};
</script>

<style lang="scss" scoped>
/* Navigation */
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 2rem;
  z-index: 1000;
  
}

.nav-menu{ 
  display: flex;
  justify-content: space-between;
  align-items: center;
  list-style: none;
  border-radius: 30px;
  gap: 2rem;
  transition: 0.3s;
}

.navbar img {
  width: 80px;
  height: auto;
}

.nav-link{
  transition: 0.3s ease;
  text-decoration: none;
  color: #384b47;
}

.nav-link:hover{
  color: #384b47;
}

.nav-menu.active{
  left: 0;
  padding: 1em ;
}

.hamburger{
  display: none;
}

@media (max-width: 768px){
  /* Navigation */
  .nav-menu{
    position: absolute;
    top: 0;
    left: -100%;
    background-color: var(--clr-Black);
    width: 100%;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 0;
    transition: 0.3s;
  }

  .nav-item{
    margin: 1em 0;
  }

  .hamburger{
    position: relative;
    display: block;
    cursor: pointer;
    z-index: 500;
    transition: 0.3s;
  }

  .hamburger.active .bar:nth-child(2){
    opacity: 0;
  }
  .hamburger.active .bar:nth-child(1){
    transform: translateY(8px) rotate(45deg);
  }
  .hamburger.active .bar:nth-child(3){
    transform: translateY(-8px) rotate(-45deg);
  }

  .bar{
    z-index: 550;
    display: block;
    width: 25px;
    height: 3px;
    margin: 5px auto;
    -webkit-transition: all 0.3s ease-in-out;
    transition: all 0.3s ease-in-out;
    background-color: var(--clr-White, #fff);
  }
}
</style>
