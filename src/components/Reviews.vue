<template>
     <section class="reviews" id="reviews">
        <div class="grid-con">
            <div class="review-heading col-span-full">
                <h2>What Clients Say</h2>
                <div class="divisor">
                </div>
            </div>
            <div class="review-con col-span-full">
                <div class="review-card" v-for="review in paginatedReviews" :key="review.id">
                    <div class="card-img">
                        <img :src="review.image" alt="reviewer image" class="reviewer-image">
                    </div>
                    <div class="card-text">
                        <h4 class="body-text-bold">{{ review.name }}</h4>
                        <p class="body-text-light">{{ review.role }}</p>
                    </div>

                    <div class="card-review-overlay">
                        <p class="body-text">{{ review.quote }}</p>
                    </div>
                </div>
                
            </div>
            <div class="pagination-controls col-span-full">
                    <button @click="currentPage--"
                    :disabled="currentPage === 1">
                        Previous
                    </button>

                    <span>Page {{ currentPage }} of {{ totalPages }}</span>
                    
                    <button @click="currentPage++"
                    :disabled="currentPage === totalPages">
                        Next
                    </button>
                </div>

        </div>
            
        </section>
</template>

<script>
import { reviewData } from '../data/reviewsData.js'

export default {
  name: 'reviews',
  data() {
    return {
      reviews: reviewData,
      currentPage: 1,
      reviewsPerPage: 4
    }
  },
  computed: {
    paginatedReviews() {
        const start = (this.currentPage - 1) * this.reviewsPerPage;
        const end = start + this.reviewsPerPage;
        return this.reviews.slice(start, end);
    },
    totalPages() {
        return Math.ceil(this.reviews.length / this.reviewsPerPage);  
    }
}
}
</script>