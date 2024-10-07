<script setup>
import { ref, onMounted } from 'vue';
import BookDetails from './BookDetails.vue';
import BooksView from './BooksViewAsList.vue';

const bookIds = ref([]);
const isLoading = ref(false);
const error = ref(null);

onMounted(() => {
  isLoading.value = true;
  fetch('http://localhost:3000/books/')
    .then(response => response.json())
    .then(data => {
      bookIds.value = data.map(book => book.id);
      isLoading.value = false;
    })
    .catch(err => {
      console.error("Failed to fetch books:", err);
      error.value = err;
      isLoading.value = false;
    });
});
</script>

<template>
  <main>
    <div v-if="isLoading">
      Loading books...
    </div>
    <div v-else-if="error">
      Failed to load books: {{ error.message }}
    </div>
    <div v-else class="container mt-3 mb-3">
      <div class="row g-3"> <!-- `g-3` adds more gap between columns -->
        <div v-for="id in bookIds" :key="id" class="col-sm-6 col-md-4 col-lg-3">
          <BookDetails :id="id" />
        </div>
      </div>
    </div>
  </main>
</template>




