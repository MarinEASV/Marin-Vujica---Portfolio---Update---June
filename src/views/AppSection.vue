<template>
  <section id="app">
    <h2 class="h2-hunt">REMOTE HUNT APP</h2>
    <div class="app-content">
      <img src="/src/assets/app .jpg" alt="App" class="app-image" />
      <div class="app-text">
        <p>Our team of 4 worked together to create a student remote jobs app. We started by talking to students to learn what they needed. Then we came up with ideas for the app and tested them to see what worked best. We listened to feedback from students to make sure the app was easy to use. Now, students can easily find remote job opportunities with our app!</p>
        <a href="https://www.figma.com/proto/MmvKeKjJvgY9pLrzl4t5pm/app?page-id=0%3A1&node-id=101-1744&scaling=scale-down&starting-point-node-id=101%3A2979&t=fUK30KbBTjHePWd0-1" class="app-link">VIEW APP PROTOTYPE</a> 
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'AppSection'
};
</script>

<style scoped>
#app {
  padding: 40px 20px;
  background-color: #d3e8d7;
  margin-bottom: 20px;
}

.app-content {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 20px;
  align-items: center;
}

.app-image {
  width: 500px;
  height: auto;
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.app-text {
  max-width: 300px;
  text-align: left;
}

.app-link {
  display: inline-block;
  margin-top: 10px;
  padding: 10px 20px;
  background-color: #384b47;
  color: #d3e8d7;
  text-decoration: none;
  transition: background-color 0.5s;
}

.app-link:hover {
  background-color: #d3e8d7;
  color: #384b47;
  border-color: #384b47;
  border-style: solid;
}
.h2-hunt {
    font-size: 30px;
    margin: 40px;
    display: flex;
    justify-content: center;
  }
</style>
