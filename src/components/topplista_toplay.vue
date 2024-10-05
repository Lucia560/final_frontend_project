
<template>
    <div id="lista_title" >
        <h2 class="topplista-title">Utforska vår topplista</h2> 
    </div>
   
    <div id="topplistaCarousel" class="carousel slide" data-bs-ride="carousel">
     <div class="carousel-inner">
        <!-- First Slide -->
        <div class="carousel-item active">
          <div class="images-container">
            <img src="@/assets/theWitcher.png" class="img-fluid" alt="Image 1">
            <img src="@/assets/theWitcher.png" class="img-fluid" alt="Image 2">
            <img src="@/assets/theWitcher.png" class="img-fluid" alt="Image 3">
            <img src="@/assets/theWitcher.png" class="img-fluid" alt="Image 4">
          </div>
        </div>
        <!-- Second Slide -->
        <div class="carousel-item">
          <div class="images-container">
            <img src="@/assets/theWitcher.png" class="img-fluid" alt="Image 5">
            <img src="@/assets/theWitcher.png" class="img-fluid" alt="Image 6">
            <img src="@/assets/theWitcher.png" class="img-fluid" alt="Image 7">
            <img src="@/assets/theWitcher.png" class="img-fluid" alt="Image 8">
          </div>
        </div>
        <!-- Additional slides can be added similarly -->
      </div>
      <!-- Controls -->
      <button class="carousel-control-prev" type="button" data-bs-target="#topplistaCarousel" data-bs-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Previous</span>
      </button>
      <button class="carousel-control-next" type="button" data-bs-target="#topplistaCarousel" data-bs-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Next</span>
      </button>
    </div>

  </template>
  
  
  <style scoped>
 
 .images-container {
  display: flex;
  justify-content: flex-start;
  align-items: center;
  gap: 5px; /* Adjust the gap as needed */
}

.images-container img {
  width: calc(25% - 5px); /* Increase the width percentage for fewer images per slide */
  height: auto; /* Maintains the aspect ratio */
  flex: 0 0 auto; /* Prevents the image from growing or shrinking beyond its set width */
}

#topplistaCarousel {
  width: 100%; /* Ensures the carousel takes the full width of its container */
  display: flex;
  align-items: center;
}

#lista_titel{
  width: 100%; /* Ensures the title takes full width */
  text-align: left; /* Aligns the title to the left */
  margin-bottom: 20px; /* Adds space below the title */
}




  </style>
  
  
  


 



  