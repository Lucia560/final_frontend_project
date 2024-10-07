<script setup>
import { ref, onMounted } from 'vue';

const book = ref({
  volumeInfo: {
    title: "Loading...",
    authors: ["Unknown"],
    description: "Data is being loaded...",
    imageLinks: {
      thumbnail: "" // A default placeholder image URL could also be used here
    },
    price: "N/A",
    categories: ["Data loading..."],
    news: false,
    amount: 0,
    favorite: false
  }
});

const props = defineProps({
  id: {
    type: String,
    required: true
  }
});

const emit = defineEmits([])

onMounted(() => {
  fetch(`http://localhost:3000/books/${props.id}`)
    .then(response => response.json())
    .then(data => {
      book.value = data; // Assume the data structure matches what you expect
    })
    .catch(error => {
      console.error('Failed to fetch book details:', error);
      book.value.volumeInfo.title = "Failed to load data";
      // Additional error handling logic can be implemented here
    });
});
</script>

<template>
  <div class="card" style="width: 14rem;">
    <div class="image-container">
      <img :src="book.volumeInfo.imageLinks.thumbnail" 
           @error="event => event.target.src = './assets/images/placeholder_image.jpg'"
           class="card-img-top book-cover" alt="Book cover">
    </div>
    <div class="card-body">
      <h5 class="card-title">{{ book.volumeInfo.title }}</h5>
      <p class="card-text">{{ book.volumeInfo.authors.join(', ') }}</p>
      <button @click="goToBookBuyForm" class="btn buy-button">
        Buy for {{ book.volumeInfo.price }}
      </button>
    </div>
  </div>
</template>

<style scoped>

h5 {
  margin: 0%;
}
.card {
  display: flex;
  flex-direction: column;
  align-items: left; /* Adjusted for left alignment */
  width: 100%; /* Adjust width as needed */
  margin: 0px;; /* Reduced space below each card, adjust as needed */
}

.image-container {
  width: 100%; /* Full width to center the image */
  display: flex;
  justify-content: center; /* Center horizontally */
  padding-top: 2px; /* Minimized padding at the top */
  margin-bottom: 2px; /* Reduce space between image and card body */
}

.book-cover {  
  height: 300px; /* Adjusted height */
  width: auto; /* Maintain aspect ratio */
  object-fit: cover; /* Ensures the image covers the area */
  margin-bottom: 0px; /* Minimize space below the image */
}

.card-body {
  display: flex;
  flex-direction: column;
  align-items: left; /* Left-align text and button */
  width: 100%;
  padding: 2px 10px; /* Reduce padding around content */
  margin-bottom: 2px; /* Minimize space at the bottom of the card body */
}
.card-text {
  margin: 0px;
}

.buy-button {
  background-color: #4a5d3c; /* Custom green color */
  border-color: #4a5d3c; /* Match border to background */
  color: white; /* Text color */
  width: 100%;
  margin-top: 2px; /* Reduce space above the button */
}

.buy-button:hover {
  background-color: darken(#4a5d3c, 10%); /* Slightly darker on hover */
  border-color: darken(#4a5d3c, 10%);
}
</style>
