<template>
    <div class="gift-card-container d-flex" style="height: 100vh;">
      <div class="gift-card-image" style="flex: 1 1 50%; height: 100%; display: flex; justify-content: center; align-items: center;">
        <img
          src="//sky-static.mavi.com/mnresize/1430/2028/2000000000046_image_9_HORIZONTAL.jpg?HORIZONTAL"
          alt="Online Hediye Kartı"
          title="Online Hediye Kartı"
          class="img-fluid"
          style="max-height: 100%; object-fit: contain;"
        />
      </div>
  
      <div class="gift-card-form" style="flex: 1 1 50%; height: 100%; padding: 3rem; display: flex; flex-direction: column; justify-content: center;">
        <h3 class="gift-card-title">Mavi Hediye Kartı</h3>
        <p class="gift-card-subtitle">En özel anlara, en güzel hediye...</p>
  
        <div class="mb-3">
          <label for="gift-card-selection" class="form-label">Hediye Kartı</label>
          <select id="gift-card-selection" class="form-select">
            <option value="online">Online Hediye Kartı</option>
          </select>
        </div>

        <div class="mb-3">
          <label for="price-selection" class="form-label">Tutar</label>
          <div>
            <button class="btn btn-outline-secondary">150 TL</button>
            <button class="btn btn-outline-secondary">350 TL</button>
            <button class="btn btn-outline-secondary">500 TL</button>
            <button class="btn btn-outline-secondary">Diğer</button>
          </div>
        </div>
  
        <div class="mb-3">
          <label for="message" class="form-label">Göndermeden önce mesajınızı eklemek ister misiniz?</label>
          <textarea id="message" class="form-control" rows="3"></textarea>
        </div>
  
        <div class="mb-3">
          <label for="email-send" class="form-check-label">
            <input type="checkbox" id="email-send" class="form-check-input" />
            Hediye kartını e-posta olarak gönder
          </label>
        </div>
  
        <div>
          <button class="btn btn-dark w-100">SEPETE EKLE</button>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: "GiftCardComponent",
  };
  </script>
  
  <style scoped>
  .gift-card-container {
    background-color: #f8f8f8;
    height: 100vh; /* Ekranın tamamını kaplamak için */
  }
  
  .gift-card-title {
    font-size: 1.8rem;
    font-weight: bold;
    margin-bottom: 0.5rem;
  }
  
  .gift-card-subtitle {
    font-size: 1rem;
    color: #555;
    margin-bottom: 1rem;
  }
  
  .gift-card-image img {
    max-width: 100%;
    height: auto;
    object-fit: contain;
  }
  
  .gift-card-form .form-select,
  .gift-card-form .form-control {
    width: 100%;
    max-width: 250px;
  }
  
  .gift-card-form .btn-outline-secondary {
    margin-right: 5px;
  }
  
  .gift-card-form button {
    font-size: 1.2rem;
    padding: 10px 20px;
  }
  </style>