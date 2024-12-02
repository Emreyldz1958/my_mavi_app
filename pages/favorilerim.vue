<template>
    <div class="product-grid d-flex flex-wrap justify-content-center">
      <div v-for="(product, index) in products" :key="index" class="product-card">
        <div
          class="product-image position-relative"
          @mouseover="product.hover = true"
          @mouseleave="product.hover = false"
        >
          <img
            :src="product.image"
            alt="product"
            class="img-fluid rounded"
          />
          <div v-if="product.hover" class="overlay d-flex flex-column justify-content-end">
            <button class="btn btn-light mb-2">Sepete Ekle</button>
            <button class="btn btn-outline-danger position-absolute top-0 end-0 m-2">
              <i class="bi bi-trash"></i>
            </button>
          </div>
        </div>
        <div class="product-info mt-2">
          <h6 class="product-title">{{ product.title }}</h6>
          <div class="product-prices">
            <span class="text-muted text-decoration-line-through">
              {{ product.oldPrice }} TL
            </span>
            <span class="text-danger fw-bold ms-2">{{ product.newPrice }} TL</span>
            <span class="text-success ms-2">{{ product.discount }}%</span>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        products: [
          {
            title: "Detroit MV91 Street Indigo Mavisi Jean Pantolon",
            oldPrice: 1299.99,
            newPrice: 779.99,
            discount: 40,
            image: "//sky-static.mavi.com/mnresize/820/1162/0011221-88680_image_1.jpg",
            hover: false,
          },
          {
            title: "Suni Kürk Detaylı Bej Suni Süet Ceket",
            oldPrice: 2599.99,
            newPrice: 1949.99,
            discount: 25,
            image: "//sky-static.mavi.com/mnresize/820/1162/0110451-70068_image_1.jpg",
            hover: false,
          },
          {
            title: "Kaşmir Karışımlı Kahverengi Kazak",
            oldPrice: 1299.99,
            newPrice: 779.99,
            discount: 40,
            image: "//sky-static.mavi.com/mnresize/820/1162/0710186-88083_image_1.jpg",
            hover: false,
          },
          {
            title: "Kapüşonlu Siyah Parka",
            oldPrice: 2599.99,
            newPrice: 1949.99,
            discount: 25,
            image: "//sky-static.mavi.com/mnresize/820/1162/0110442-71379_image_1.jpg",
            hover: false,
          },
        ],
      };
    },
  };
  </script>
  
  <style scoped>
  .product-grid {
    gap: 1.5rem;
    justify-content: center; 
    display: flex;
    flex-wrap: wrap;
    margin-top: 50px; 
  }
  .product-card {
    max-width: 250px;
  }
  .product-image {
    height: 300px;
    overflow: hidden;
    position: relative;
  }
  .overlay {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: rgba(0, 0, 0, 0.6);
    align-items: center;
    padding: 1rem;
  }
  .btn-light {
    background-color: white;
    color: black;
  }
  .position-absolute.top-0.end-0 {
    right: 10px;
    top: 10px;
  }
  .product-info {
    text-align: center;
  }
  .product-prices span {
    display: block;
  }
  </style>
  