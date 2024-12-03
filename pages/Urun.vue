<template>
    <div class="product-card p-3 border rounded">
      <div class="row">

        <div class="col-md-6 d-flex">
          <!-- İlk Resim -->
          <div class="product-image me-2">
            <img
              src="//sky-static.mavi.com/mnresize/820/1162/101437-85292_image_1.jpg"
              alt="BLISS-0"
              title="BLISS-0"
              class="img-fluid"
            />
          </div>
          <!-- İkinci Resim -->
          <div class="product-image">
            <img
              src="//sky-static.mavi.com/mnresize/820/1162/101437-85292_image_2.jpg"
              alt="BLISS-1"
              title="BLISS-1"
              class="img-fluid"
            />
          </div>
        </div>
  
        <!-- Ürün Bilgileri -->
        <div class="col-md-6 d-flex flex-column">
          <h2 class="product-title">Bliss Mavi Premium Koyu Mavi Jean Pantolon</h2>
          <p class="product-category">Flare - Bootcut, Yüksek Bel, İspanyol Paça</p>
  
          <!-- Fiyat Alanı -->
          <div class="product-pricing">
            <p class="text-muted text-decoration-line-through">1.199,99 TL</p>
            <p class="text-danger fw-bold">899,99 TL</p>
            <span class="badge bg-danger">-25%</span>
          </div>
  
          <!-- Renk Seçenekleri -->
          <div class="product-colors my-2">
            <label class="form-label">Renk Seçenekleri:</label>
            <div class="d-flex align-items-center">
              <!-- Renk Düğmeleri -->
              <div class="color-circle me-2" style="background-color: #2c3e50;" title="Koyu Mavi"></div>
              <div class="color-circle me-2" style="background-color: #37474f;" title="Gri Mavi"></div>
              <div class="color-circle me-2" style="background-color: #1e272e;" title="Siyah"></div>
              <span class="ms-2 text-muted">+1 Renk</span>
            </div>
          </div>
  
          <!-- Dropdown Menüsü -->
          <div class="product-size my-2">
            <label for="size-select" class="form-label">Beden / Boy Seç</label>
            <select id="size-select" class="form-select">
              <option>Beden Seç</option>
              <option>32</option>
              <option>34</option>
              <option>36</option>
            </select>
          </div>
  
          <!-- Butonlar -->
          <div class="product-buttons mt-3">
            <button class="btn btn-dark w-100 mb-2">Sepete Ekle</button>
            <button class="btn btn-outline-secondary w-100 mb-2">Kombini İncele</button>
            <button class="btn btn-outline-secondary w-100">Mağazada Bul</button>
          </div>
  
          <!-- Ürün Detayları -->
          <div class="product-details mt-3">
            <h5>Ürün Özellikleri</h5>
            <ul>
              <li><strong>Kumaş Bilgileri:</strong> %95 Pamuk, %3 Elastomultiester, %2 Elastan</li>
              <li><strong>Manken Ölçüleri:</strong></li>
              <ul>
                <li>Bel: 26 / Boy: 32</li>
                <li>Boy: 180 cm</li>
                <li>Bel: 60 cm / Göğüs: 81 cm / Kalça: 88 cm</li>
              </ul>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: "ProductCard",
  };
  </script>
  
  <style scoped>
  .product-image {
    width: 50%; 
  }
  
  .product-title {
    font-size: 1.5rem;
    font-weight: bold;
  }
  
  .product-pricing p {
    margin: 0;
  }
  
  .color-circle {
    width: 20px;
    height: 20px;
    border-radius: 50%;
    border: 1px solid #ccc;
    cursor: pointer;
  }
  .product-details ul {
    padding-left: 1rem;
    list-style-type: disc;
  }
  .product-details ul ul {
    padding-left: 1.5rem;
    list-style-type: circle;
  }
  </style>