<template>
    <section id="photography">
      <h2 class="h2-photo">PHOTOGRAPHY</h2>
      <div class="photos-container">
        <img v-for="photo in photos" :key="photo.id" :src="photo.imageUrl" :alt="photo.title" class="photo" />
      </div>
      <div class="photo-text">
          <p>I really enjoy taking pictures outdoors as a hobby. It's something I love doing, and it has actually helped me get interested in graphic design as a job. When I take photos outside, I started playing around with editing them on my computer. This got me thinking more about how things look and fit together in a picture. Eventually, I realized I wanted to explore graphic design more because it lets me be creative in a similar way to taking photos. It's been a smooth transition from just enjoying photography to wanting to do design as a career.</p>
        </div>
    </section>
  </template>
  
  <script>
  import photo1 from '/src/assets/20210228_141049.jpg';
  import photo2 from '/src/assets/20230905_200110.jpg';
  import photo3 from '/src/assets/1609694638576.jpg';
  import photo4 from '/src/assets/1693136953010.jpg';
  
  export default {
    name: 'PhotographySection',
    data() {
      return {
        photos: [
          { id: 1, title: 'Photo 1', imageUrl: photo1 },
          { id: 2, title: 'Photo 2', imageUrl: photo2 },
          { id: 3, title: 'Photo 3', imageUrl: photo3 },
          { id: 4, title: 'Photo 4', imageUrl: photo4 },
        ]
      };
    }
  };
  </script>
  
  <style scoped>
  #photography {
    padding: 40px 20px;
    background-color: #d3e8d7;
  }
  
  .photos-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 20px;
  }
  
  .photo {
    width: 300px;
    height: auto;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  }

  .photo-text {
  margin-top: 30px;
  max-width: 670px; 
  margin-left: auto;
  margin-right: auto;
  text-align: center; 
}


  .h2-photo {
    font-size: 30px;
    margin: 20px;
    display: flex;
    justify-content: center;
  }
  
  </style>
  