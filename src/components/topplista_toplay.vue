<template>
   <div class="top-list-wrapper"> <!-- Flex container -->
    <h2 class="topplista-title">Utforska vår <span style="font-weight: bold" >Topplista</span></h2> 
 

<div id="carouselExampleControls" class="carousel slide" data-bs-ride="carousel">
    
  <div class="carousel-inner">
     
    <div class="carousel-item active">
        
     <div class="cards-wrapper">
        <div class="card" style="width: 12em;">
          <div class="image-wrapper">
  <img src="@/assets/theWitcher.png"   alt="...">
         </div>
  <div class="card-body">
    <h5 class="card-title">Card title</h5>
    <a href="#" class="btn btn-primary">Mer info</a>
  </div>
</div>

<div class="card" style="width: 12rem;">
    <div class="image-wrapper">
  <img src="@/assets/theWitcher.png"   alt="...">
    </div>
  <div class="card-body">
    <h5 class="card-title">Card title</h5>
    <a href="#" class="btn btn-primary">Mer info</a>
  </div>
</div>
      
<div class="card" style="width: 12rem;">
    <div class="image-wrapper">
  <img src="@/assets/theWitcher.png"  alt="...">
    </div>
  <div class="card-body">
    <h5 class="card-title">Card title</h5>
    <a href="#" class="btn btn-primary">Mer info</a>
  </div>
</div>

<div class="card" style="width: 12rem;">
    <div class="image-wrapper">
  <img src="@/assets/theWitcher.png"   alt="...">
    </div>
  <div class="card-body">
    <h5 class="card-title">Card title</h5>
    <a href="#" class="btn btn-primary">Mer info</a>
  </div>
</div>



   </div>
    </div>
    <div class="carousel-item">
     <div class="cards-wrapper">
        <div class="card" style="width: 12rem;">
        <div class="image-wrapper">
  <img src="@/assets/theWitcher.png" alt="...">
        </div>
  <div class="card-body">
    <h5 class="card-title">Card title</h5>
    <a href="#" class="btn btn-primary">Mer info</a>
  </div>
</div>

<div class="card" style="width: 12rem;">
    <div class="image-wrapper">
  <img src="@/assets/theWitcher.png"   alt="...">
    </div>
  <div class="card-body">
    <h5 class="card-title">Card title</h5>
    <a href="#" class="btn btn-primary">Mer info</a>
  </div>
</div>


<div class="card" style="width: 12rem;">
    <div class="image-wrapper">
  <img src="@/assets/theWitcher.png"  alt="...">
    </div>
  <div class="card-body">
    <h5 class="card-title">Card title</h5>
    <a href="#" class="btn btn-primary">Mer info</a>
  </div>
</div>

<div class="card" style="width: 12rem;">
    <div class="image-wrapper">
  <img src="@/assets/theWitcher.png"   alt="...">
    </div>
  <div class="card-body">
    <h5 class="card-title">Card title</h5>
    <a href="#" class="btn btn-primary">Mer info</a>
  </div>
</div>



   </div>    
    </div>
    <div class="carousel-item">
     <div class="cards-wrapper">

        <div class="card" style="width: 12rem;">
            <div class="image-wrapper">
  <img src="@/assets/theWitcher.png"  alt="...">
            </div>
  <div class="card-body">
    <h5 class="card-title">Card title</h5>
    <a href="#" class="btn btn-primary">Mer info</a>
  </div>
</div>

<div class="card" style="width: 12rem;">
    <div class="image-wrapper">
  <img src="@/assets/theWitcher.png"   alt="...">
    </div>
  <div class="card-body">
    <h5 class="card-title">Card title</h5>
    <a href="#" class="btn btn-primary">Mer info</a>
  </div>
</div>

<div class="card" style="width: 12rem;">
    <div class="image-wrapper">
  <img src="@/assets/theWitcher.png"   alt="...">
    </div>
  <div class="card-body">
    <h5 class="card-title">Card title</h5>
    <a href="#" class="btn btn-primary">Mer info</a>
  </div>
</div>

<div class="card" style="width: 12rem;">
    <div class="image-wrapper">
  <img src="@/assets/theWitcher.png"   alt="...">
    </div>
  <div class="card-body">
    <h5 class="card-title">Card title</h5>
    <a href="#" class="btn btn-primary">Mer info</a>
  </div>
</div>





     </div>
      
    </div>
  </div>
  <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleControls" data-bs-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    <span class="visually-hidden">Previous</span>
  </button>
  <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleControls" data-bs-slide="next">
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
    <span class="visually-hidden">Next</span>
  </button>
</div>

   </div>
</template>

  
<style scoped>
.top-list-wrapper {
  display: flex;       /* Enables flexbox */
  align-items: center; /* Vertically centers the items in the container */
  justify-content: space-between; /* Spaces the title and carousel apart */
  width: 100%;         /* Takes full width of its parent */
  margin-top: 275px;
}

.topplista-title {
  flex: 1;             /* Allows the title to grow and take necessary space */
  margin-right: 20px;  /* Optional: Adds some space between the title and the carousel */
}

#carouselExampleControls{
  /* Reduces the maximum width of the carousel to 80% of its container */
  margin-left: 200px; /* Centers or pushes the carousel based on the margin-right value */
  flex: 3;             /* Allows the carousel to grow and take larger space */
  max-width: 80%; 
  }

 .cards-wrapper{
    display: flex;
    justify-content: center; /* Ensures cards are centered within the carousel item */
    flex-wrap: nowrap; /* Keeps all cards on a single line without wrapping */
 }

 .card{
    margin: 0 .5em;
    width: calc(100%/4);
    margin: 10px; /* Adjusts margin for spacing between cards */
    flex: 0 0 200px; /* Sets each card to have a flex-basis of 250px, adjust as needed */
 }
 .image-wrapper{
    display: flex;
    align-items: center;
    justify-content: center;
    height: 180px; /* Adjusts the height of the image container */
    width: 100%; /* Uses the full width of the card for the image */
 
 }

 .image-wrapper img{
   max-height:100%;
   max-width: 100%;
 }

 </style>
  
  




  