<template>
    <div class="container my-4">
      <div class="mb-4">
        <h5>Değerlendirmeler</h5>
        <div class="d-flex align-items-center">
          <h2 class="mb-0">4.3</h2>
          <div class="ms-2">
            <div class="text-warning">
              <i class="bi bi-star-fill"></i>
              <i class="bi bi-star-fill"></i>
              <i class="bi bi-star-fill"></i>
              <i class="bi bi-star-fill"></i>
              <i class="bi bi-star-half"></i>
            </div>
            <small>(71 Değerlendirme)</small>
          </div>
        </div>
        <div class="mt-3">
          <h6>Beden</h6>
          <div class="d-flex align-items-center">
            <small class="me-2">Dar</small>
            <div class="progress flex-grow-1" style="height: 8px;">
              <div class="progress-bar bg-secondary" role="progressbar" :style="{ width: '50%' }"></div>
            </div>
            <small class="ms-2">Geniş</small>
          </div>
        </div>
      </div>
  
      <div v-for="(review, index) in reviews" :key="index" class="card p-3 mb-3">
        <div class="d-flex align-items-center">
          <div
            class="rounded-circle bg-secondary text-white d-flex justify-content-center align-items-center"
            style="width: 40px; height: 40px;"
          >
            {{ review.initials }}
          </div>
          <div class="ms-3">
            <h6 class="mb-0">{{ review.rating }}</h6>
            <small>{{ review.date }}</small>
          </div>
        </div>
        <div class="mt-3">
          <h6>Beden</h6>
          <div class="d-flex align-items-center">
            <small class="me-2">Dar</small>
            <div class="progress flex-grow-1" style="height: 8px;">
              <div class="progress-bar bg-secondary" role="progressbar" :style="{ width: review.size + '%' }"></div>
            </div>
            <small class="ms-2">Geniş</small>
          </div>
        </div>
        <small class="mt-2 d-block">Satın aldığı ürün: Beden: {{ review.sizeLabel }}</small>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: "RatingCard",
    data() {
      return {
        reviews: [
          {
            initials: "Pi",
            rating: 5.0,
            date: "28 Kasım 2024",
            size: 50,
            sizeLabel: "L",
          },
          {
            initials: "DU",
            rating: 4.0,
            date: "13 Kasım 2024",
            size: 75,
            sizeLabel: "M",
          },
        ],
      };
    },
  };
  </script>
  