<script setup>
import { ref, onMounted } from 'vue';

const books = ref([]);  // Define reactive data with ref

// Function to fetch books from server
const fetchBooks = () => {
  fetch('http://localhost:3000/books')
    .then(res => res.json())
    .then(data => books.value = data)  // Update the reactive variable directly
    .catch(error => console.log(error.message));  // Log any errors
};

onMounted(() => {
  fetchBooks();  // Fetch books when component is mounted
});
</script>

<template>
    <div>
    <h1>Books</h1>
    <ul>
      <li v-for="book in books" :key="book.id">
        <h2>{{ book.volumeInfo.title }}</h2>
        <p>Author: {{ book.volumeInfo.authors.join(', ') }}</p>
        <p>Description: {{ book.volumeInfo.description }}</p>
        <img class="book-cover" :src="book.volumeInfo.imageLinks.thumbnail" alt="Book cover" 
        @error="event => event.target.src = './assets/images/placeholder_image.jpg'"
         />         
        <p>Price: {{ book.volumeInfo.price }}</p>
      </li>
    </ul>
  </div>
</template>