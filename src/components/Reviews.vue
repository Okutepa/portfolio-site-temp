<template>
     <section class="reviews" id="reviews">
        <div class="grid-con">
            <div class="review-heading col-span-full">
                <h2>What Clients Say</h2>
                <div class="divisor">
                </div>
            </div>
            <div class="review-con col-span-full">
                <div class="review-card" v-for="review in reviews" :key="review.id">
                    <div class="card-img">
                        <img :src="review.image" alt="reviewer image" class="reviewer-image">
                    </div>
                    <div class="card-text">
                        <h4 class="body-text-bold">{{ review.name }}</h4>
                        <p class="body-text-light">{{ review.role }}</p>
                    </div>

                </div>
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
      reviews: reviewData
    }
  }
}
</script>