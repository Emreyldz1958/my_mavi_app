<template>
    <div class="d-flex justify-content-center align-items-center vh-100">
      <div class="card p-4 shadow d-flex flex-row" style="max-width: 800px; width: 100%;">
        <div class="me-4">
          <img
            src="https://sky-static.mavi.com/mnresize/820/1162/1600361-82054_image_1.jpg"
            alt="Ürün Görseli"
            style="width: 150px; height: auto; object-fit: cover; border-radius: 8px;"
          />
        </div>
  

        <div class="flex-grow-1">
          <h4 class="text-center mb-4">Ölçüleriniz</h4>
          <p class="text-center">
            Size benzer insanların verilerine göre size en uygun bedeni bulun:
          </p>
  
  
          <div class="mb-3">
            <label for="heightInput" class="form-label">BOY</label>
            <div class="d-flex align-items-center">
              <input
                type="number"
                id="heightInput"
                class="form-control me-2"
                placeholder="Boyunuzu girin"
              />
              <div class="btn-group" role="group">
                <button
                  type="button"
                  class="btn btn-outline-success"
                  :class="{ active: unitHeight === 'cm' }"
                  @click="unitHeight = 'cm'"
                >
                  cm
                </button>
                <button
                  type="button"
                  class="btn btn-outline-success"
                  :class="{ active: unitHeight === 'in' }"
                  @click="unitHeight = 'in'"
                >
                  in
                </button>
              </div>
            </div>
          </div>
  

          <div class="mb-3">
            <label for="weightInput" class="form-label">KİLO</label>
            <div class="d-flex align-items-center">
              <input
                type="number"
                id="weightInput"
                class="form-control me-2"
                placeholder="Kilonuzu girin"
              />
              <div class="btn-group" role="group">
                <button
                  type="button"
                  class="btn btn-outline-success"
                  :class="{ active: unitWeight === 'kg' }"
                  @click="unitWeight = 'kg'"
                >
                  kg
                </button>
                <button
                  type="button"
                  class="btn btn-outline-success"
                  :class="{ active: unitWeight === 'lbs' }"
                  @click="unitWeight = 'lbs'"
                >
                  lbs
                </button>
              </div>
            </div>
          </div>
  
          <button type="button" class="btn btn-primary w-100">
            Devam <i class="bi bi-arrow-right"></i>
          </button>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        unitHeight: "cm", 
        unitWeight: "kg", 
      };
    },
  };
  </script>
  