<template>
    <section id="flyer">
      <h2 class="h2-flyer">FLYER</h2>
      <div class="flyer-content">
        <img src="/src/assets/FLYER.jpg" alt="Flyer" class="flyer-image" />
        <div class="flyer-text">
           <p>Me and another student worked together on a project using Adobe InDesign to make a flyer about one part of the Esbjerg. We made a cool flyer for the area called Saedding in our city. First, we came up with ideas and thought about who would see the flyer. Then, we used InDesign to create it, trying out different tools until it looked just right. We got feedback from each other and made changes until the flyer looked proffesional and good. We also had to use our own photos and think how to organize it with proper content. It was a fun way to learn about InDesign and make something cool for our city!</p>
           <a href="https://indd.adobe.com/view/2f04ccab-ca61-415d-87d2-07a453718cff" class="app-link">READ THE FLYER</a> 
       </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'FlyerSection'
  };
  </script>
  
  <style scoped>
  #flyer {
    padding: 40px 20px;
    background-color: #d3e8d7;
  }
  
  .flyer-content {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 20px;
    align-items: center;
  }
  
  .flyer-image {
    width: 650px;
    height: auto;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  }
  
  .flyer-text {
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
.h2-flyer {
    font-size: 30px;
  }
  </style>
  