<template>
    <div class="container mt-5">
      <h3 class="mb-4">Sepet</h3>
      <div class="row">
        <div class="col-lg-8">
          <div class="table-responsive">
            <div class="table">
              <div class="d-flex bg-light fw-bold">
                <div class="col-4 py-2">ÜRÜN</div>
                <div class="col-2 py-2">BİRİM FİYAT</div>
                <div class="col-2 py-2">ADET</div>
                <div class="col-2 py-2">TOPLAMI</div>
                <div class="col-2 py-2 text-end"></div>
              </div>
              <div class="d-flex align-items-center border-bottom py-3">
                <div class="col-4 d-flex">
                  <img
                    src="/images/image_sepset.png"
                    alt="Ürün Resmi"
                    class="me-3 rounded"
                    style="width: 70px; height: 70px; object-fit: cover;"
                  />
                  <div>
                    <p class="mb-1">Suni Deri Blazer Ceket</p>
                    <small>Beden: S</small>
                  </div>
                </div>
                <div class="col-2">2.499,99 TL</div>
                <div class="col-2">
                  <div class="input-group">
                    <button
                      class="btn btn-outline-secondary btn-sm"
                      @click="decreaseQuantity"
                    >
                      -
                    </button>
                    <input
                      type="number"
                      class="form-control text-center"
                      :value="quantity"
                      readonly
                    />
                    <button
                      class="btn btn-outline-secondary btn-sm"
                      @click="increaseQuantity"
                    >
                      +
                    </button>
                  </div>
                </div>
                <div class="col-2">
                  <div>
                    <del>2.499,99 TL</del>
                  </div>
                  <div>1.874,99 TL</div>
                  <small class="text-danger">Kazancınız 625 TL</small>
                </div>
                <div class="col-2 text-end">
                  <button class="btn btn-danger btn-sm" @click="removeItem">
                    Sil
                  </button>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="col-lg-4">
          <div class="border p-4">
            <h5>Sepet Toplamı</h5>
            <div class="d-flex justify-content-between">
              <span>Sipariş Toplamı:</span>
              <span>2.499,99 TL</span>
            </div>
            <div class="d-flex justify-content-between">
              <span>Ürün İndirimi:</span>
              <span class="text-danger">-625,00 TL</span>
            </div>
            <div class="d-flex justify-content-between">
              <span>Ara Toplam:</span>
              <span>1.874,99 TL</span>
            </div>
            <div class="d-flex justify-content-between">
              <span>Kargo:</span>
              <span>Ücretsiz</span>
            </div>
            <hr />
            <div class="d-flex justify-content-between fw-bold">
              <span>Toplam:</span>
              <span>1.874,99 TL</span>
            </div>
            <button class="btn btn-dark w-100 mt-3">Satın Al</button>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        quantity: 1, 
      };
    },
    methods: {
      increaseQuantity() {
        this.quantity++;
      },
      decreaseQuantity() {
        if (this.quantity > 1) {
          this.quantity--;
        }
      },
      removeItem() {
        alert("Ürün sepetten kaldırıldı!");
      },
    },
  };
  </script>
  