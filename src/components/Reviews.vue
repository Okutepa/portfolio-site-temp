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
                        <img src="" alt="">

                    </div>
                    <div class="card-text">
                        <h4>Jade A.</h4>
                        <p>Content Strategist</p>
                    </div>
                </div>

                <div class="review-card">
                    <div class="card-img">
                        <img src="" alt="">

                    </div>
                    <div class="card-text">
                        <h4>Jade A.</h4>
                        <p>Content Strategist</p>
                    </div>
                </div>

                <div class="review-card">
                    <div class="card-img">
                        <img src="" alt="">

                    </div>
                    <div class="card-text">
                        <h4>Jade A.</h4>
                        <p>Content Strategist</p>
                    </div>
                </div>

                <div class="review-card">
                    <div class="card-img">
                        <img src="" alt="">

                    </div>
                    <div class="card-text">
                        <h4>Jade A.</h4>
                        <p>Content Strategist</p>
                    </div>
                </div>

                <div class="pagination">

                </div>
            </div>

        </div>
            
        </section>
</template>

<script>

import { reviewData } from '../data/reviewsData.js'

export default {
  name: 'Reviews',
  data() {
    return {
      reviews: reviewData
    }
  }
}
</script>