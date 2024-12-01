<template>
    <!-- Navbar'ın yüksekliğinden dolayı formu aşağıdan başlatmak için pt-5 ekledik -->
    <div class="d-flex justify-content-center align-items-center vh-100" style="margin-top: 80px;">
      <div class="container p-4" style="max-width: 500px;">
        <h3 class="text-center mb-4">Üye Ol</h3>
        <form>
          <!-- Ad ve Soyad -->
          <div class="row mb-3">
            <div class="col-md-6">
              <input
                type="text"
                class="form-control"
                placeholder="Ad"
                required
              />
            </div>
            <div class="col-md-6">
              <input
                type="text"
                class="form-control"
                placeholder="Soyadı"
                required
              />
            </div>
          </div>
          <!-- Telefon -->
          <div class="mb-3">
            <input
              type="tel"
              class="form-control"
              placeholder="Telefon"
              required
            />
          </div>
          <!-- Doğum Tarihi -->
          <div class="row mb-3">
            <div class="col-md-4">
              <select class="form-select" required>
                <option selected>Gün</option>
                <option v-for="day in 31" :key="day" :value="day">
                  {{ day }}
                </option>
              </select>
            </div>
            <div class="col-md-4">
              <select class="form-select" required>
                <option selected>Ay</option>
                <option v-for="(month, index) in months" :key="index" :value="month">
                  {{ month }}
                </option>
              </select>
            </div>
            <div class="col-md-4">
              <select class="form-select" required>
                <option selected>Yıl</option>
                <option v-for="year in years" :key="year" :value="year">
                  {{ year }}
                </option>
              </select>
            </div>
          </div>
          <!-- Cinsiyet -->
          <div class="mb-3">
            <select class="form-select" required>
              <option selected>Cinsiyet</option>
              <option value="Erkek">Erkek</option>
              <option value="Kadın">Kadın</option>
              <option value="Diğer">Diğer</option>
            </select>
          </div>
          <!-- E-posta -->
          <div class="mb-3">
            <input
              type="email"
              class="form-control"
              placeholder="E-Posta Adresi"
              required
            />
          </div>
          <!-- Şifre -->
          <div class="mb-3 position-relative">
            <input
              type="password"
              class="form-control"
              placeholder="Şifre"
              required
            />
            <button
              type="button"
              class="btn btn-sm btn-outline-secondary position-absolute"
              style="top: 0; right: 10px;"
            >
              👁
            </button>
          </div>
          <!-- Aydınlatma ve Onay -->
          <div class="mb-3">
            <small>
              Lütfen üye olmadan önce <a href="#">Aydınlatma Metni</a>'ni okuyunuz.
            </small>
          </div>
          <div class="form-check mb-2" v-for="(text, index) in checkboxes" :key="index">
            <input
              type="checkbox"
              class="form-check-input"
              :id="'checkbox-' + index"
              required
            />
            <label class="form-check-label" :for="'checkbox-' + index">
              {{ text }}
            </label>
          </div>
          <!-- Üyelik Sözleşmesi -->
          <div class="form-check mb-4">
            <input
              type="checkbox"
              class="form-check-input"
              id="contract"
              required
            />
            <label class="form-check-label" for="contract">
              Üyelik sözleşmesi'ni okudum, kabul ediyorum.
            </label>
          </div>
          <!-- Üye Ol Butonu -->
          <button type="submit" class="btn btn-dark w-100">Üye Ol</button>
          <p class="text-center mt-3">veya</p>
          <button type="button" class="btn btn-outline-primary w-100">
            Facebook ile Üye Ol
          </button>
        </form>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        months: [
          "Ocak",
          "Şubat",
          "Mart",
          "Nisan",
          "Mayıs",
          "Haziran",
          "Temmuz",
          "Ağustos",
          "Eylül",
          "Ekim",
          "Kasım",
          "Aralık",
        ],
        years: Array.from({ length: 100 }, (_, i) => new Date().getFullYear() - i),
        checkboxes: [
          "Mavi Giyim Sanayi ve Ticaret A.Ş.'nin tarafıma SMS ile ticari elektronik ileti göndermesine burada belirtilen izinleri veriyorum.",
          "Mavi Giyim Sanayi ve Ticaret A.Ş.'nin tarafıma e-posta ile ticari elektronik ileti göndermesine burada belirtilen izinleri veriyorum.",
          "Kişisel verilerimin kişiselleştirilmiş pazarlama, profilleme/segmentasyon amacıyla işlenmesine ilişkin Açık Rıza metnini okudum, kabul ediyorum.",
        ],
      };
    },
  };
  </script>
  