<template>
  <div class="d-flex justify-content-center align-items-center vh-100">
    <div class="container" style="max-width: 500px;">
      <div class="row justify-content-center">
        <div class="col-md-12">
          <div class="d-flex justify-content-between border-bottom pb-3 mb-4">
            <button
              class="btn btn-link text-dark fw-bold px-0"
              :class="{ 'border-bottom border-dark fw-bold': isLoginActive }"
              @click="isLoginActive = true"
            >
              Giriş Yap
            </button>
            <button
              class="btn btn-link text-dark fw-bold px-0"
              :class="{ 'border-bottom border-dark fw-bold': !isLoginActive }"
              @click="isLoginActive = false"
            >
              Üye Ol
            </button>
          </div>

          <form>
            <div class="mb-3">
              <label for="email" class="form-label visually-hidden">E-Posta Adresi / Telefon Numarası</label>
              <input
                type="email"
                id="email"
                class="form-control border-0 border-bottom"
                placeholder="E-Posta Adresi / Telefon Numarası"
              />
            </div>

            <div class="mb-3 position-relative">
              <label for="password" class="form-label visually-hidden">Şifre</label>
              <div class="input-group border-0 border-bottom">
                <input
                  :type="passwordVisible ? 'text' : 'password'"
                  id="password"
                  class="form-control border-0"
                  placeholder="Şifre"
                />
                <button
                  type="button"
                  class="btn btn-outline-secondary border-0 bg-white"
                  @click="passwordVisible = !passwordVisible"
                >
                  <i :class="passwordVisible ? 'bi bi-eye' : 'bi bi-eye-slash'"></i>
                </button>
              </div>
            </div>

            <div class="text-end mb-4">
              <a href="#" class="text-decoration-none">Şifremi Unuttum</a>
            </div>

            <button type="submit" class="btn btn-dark w-100 mb-3">Giriş Yap</button>

            <div class="text-center mb-3">veya</div>

            <button type="button" class="btn btn-outline-primary w-100">
              Facebook ile Giriş Yap
            </button>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isLoginActive: true,
      passwordVisible: false, 
    };
  },
};
</script>
