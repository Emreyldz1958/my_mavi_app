ahmet coban, [3.12.2024 21:12]
<template>
  <header>
    <!-- Üst Kısım: Mavi Logo Container -->
    <div class="logo-container">
      <a href="#" class="navbar-brand">
        <img src="/images/mavi-logo.svg" alt="Mavi" title="Mavi" class="mavi-logo" />
      </a>
    </div>

    <!-- Navbar Container -->
    <nav class="navbar navbar-expand-lg">
      <div class="container">
        <!-- Sol Taraf: Menü Ögeleri -->
        <div class="navbar-left">
          <ul class="navbar-nav">
            <li class="nav-item"><a class="nav-link" href="#">Jean</a></li>
            <li class="nav-item"><a class="nav-link" href="#">Kadın</a></li>
            <li class="nav-item"><a class="nav-link" href="#">Erkek</a></li>
            <li class="nav-item"><a class="nav-link" href="#">Çocuk</a></li>
            <li class="nav-item"><a class="nav-link" href="#">All Blue</a></li>
            
            <li
              class="nav-item"
              @mouseenter="showRedContainer"
              @mouseleave="hideRedContainer($event)"
              >
              <a class="nav-link" href="#">Outlet</a>
            </li>


            <li class="nav-item"><a class="nav-link" href="#">Hediye Kartı</a></li>
            <li class="nav-item"><a class="nav-link" href="#">Kartuş</a></li>
          </ul>
        </div>

        <!-- Sağ Taraf: Arama Çubuğu ve İkonlar -->
        <div class="navbar-right">
          <div class="search-container">
            <input type="text" class="search-input" placeholder="Arama yap..." />
            <button class="search-btn">
              <i class="bi bi-search"></i>
            </button>
          </div>
          <div class="navbar-icons">
            <a href="#" class="nav-icon"><i class="bi bi-heart"></i></a>
            <a href="#" class="nav-icon"><i class="bi bi-person"></i></a>
            <a href="#" class="nav-icon"><i class="bi bi-bag"></i></a>
          </div>
        </div>
      </div>
    </nav>
  </header>

   <!-- Yeni Kırmızı Container -->
  <div
    class="red-container"
    v-show="isRedContainerVisible"
    @mouseenter="keepRedContainerVisible"
    @mouseleave="hideRedContainer($event)"
  >
    <div class="container" v-show="isRedContainerVisible">
      <div class="row">
        <!-- Sütunlar -->
        <div class="col-12 col-md-2" v-for="(column, index) in columns" :key="index">
          <!-- Başlık -->
          <h5>
            <a href="#" class="column-title text-decoration-none">{{ column.title }}</a>
          </h5>
          <!-- Satırlar -->
          <ul class="list-unstyled">
            <li v-for="(item, idx) in column.items" :key="idx">
              <a href="#" class="text-decoration-none text-dark">{{ item }}</a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
  
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  data() {
    return {
      isRedContainerVisible: false as boolean, 
      columns: [
        { title: "Kadın", items: ["Jean", "Switsheart", "Tişört", "Basic"] },
        { title: "Aksesuar", items: ["Çanta-Cüzdan", "Çorap", "Şal-Atkı", "Bere"] },
        { title: "Erkek", items: ["Jean", "Switsheart", "Tişört", "Basic"] },
        { title: "Aksesuar", items: ["Boxer", "Çorap", "Kemer", "Çanta"] },
        { title: "Çocuk", items: ["Tüm Kız Çocuk Ürünleri", "Tişört", "Tüm Erkek Çocuk Ürünleri", "Jean"] },
      ],
    };
  },
  methods: {
    showRedContainer(): void {
      console.log("Show red container"); 
      this.isRedContainerVisible = true; 
    },
    hideRedContainer(event: MouseEvent): void {
    const relatedTarget = event.relatedTarget as HTMLElement;
    const redContainer = document.querySelector(".red-container");
    const outletNavItem = document.querySelector(".nav-item a[href='#']");

    // Eğer fare, kırmızı container veya "Outlet" linkinin üzerindeyse gizleme.
    if (
      redContainer?.contains(relatedTarget) ||
      outletNavItem?.contains(relatedTarget)
    ) {
      return;
    }
    this.isRedContainerVisible = false;
    },
    keepRedContainerVisible(): void {
      console.log("Keep red container visible"); // Debug
      this.isRedContainerVisible = true; // Kırmızı container üzerinde kalındığında görünür kalmaya devam et
    },
  },
});
</script>



<style scoped>
body {
  font-weight: 400; 
}

/* Üst Kısım: Logo */
.logo-container {
  background-color: white;
  padding: 10px 0; 
  text-align: center;
  border-bottom: 1px solid #ddd; 
  margin-top: -20px; 
}

.mavi-logo {
  height: 50px; 
}


/* Navbar */
.navbar {
  background-color: white;
  border-bottom: 0.5px solid #ddd; 
}

/* Sol Taraftaki Navbar Öğeleri */
.navbar-left {
  display: flex;
  flex: 1;
  justify-content: flex-start; 
  margin-left: -250px; 
}

.navbar-nav {
  display: flex;
  justify-content: flex-start;
  flex-grow: 1;
  margin-left: 0; 
}

.navbar-nav .nav-item {
  position: relative; 
}

.navbar-nav .nav-item::after {
  content: '';
  position: absolute;
  top: -10px; 
  bottom: -10px;
  left: -10px; 
  right: -10px;
}

.navbar-nav .nav-link {
  color: #000;
  font-weight: 400; 
  font-size: 18px; 
  padding: 10px 15px;
}

/* Sağ Taraf: Arama Çubuğu ve İkonlar */
.navbar-right {
  display: flex;
  justify-content: flex-end; 
  align-items: center;
  gap: 10px; 
  margin-right: -200px; 
}

.search-container {
  display: flex;
  align-items: center;
  margin-right: 10px; 
  position: relative;
}

.search-input {
  padding: 10px 15px;
  font-size: 16px;
  width: 250px;
  border: none;
  border-bottom: 1.5px solid #000;
  padding-right: 35px; 
}

.search-btn {
  position: absolute;
  right: 10px;
  top: 50%;
  transform: translateY(-50%);
  background: none;
  border: none;
  color: #000;
  font-size: 20px; 
  cursor: pointer;
}

/* Navbar İkonları */
.navbar-icons {
  display: flex;
  margin-left: 0; 
  gap: 10px; 
}

.navbar-icons .nav-icon {
  color: #000;
  font-size: 22px; 
  text-decoration: none;
}

/* Yeni Kırmızı Container */
.red-container {
  background-color: white;
  width: 100%;
  height: 20vw; 
  margin-top: 1px; 
  border-bottom: 3px solid #000;

}

.red-container a {
  color: #000; 
}

.red-container .container {
  margin-left: 42px; 
}

.red-container .row {
  justify-content: flex-start; 
}

.column-title {
  font-weight: bold;
  color: white;
}

.column-title:hover {
  text-decoration: underline;
}

.red-container[v-cloak] {
  display: none; /* Vue işlemleri sırasında görünmez */
}

/* Responsive Tasarım */
@media (max-width: 768px) {
  .navbar-left {
    display: block;
    text-align: center;
  }

  .navbar-right {
    display: block;
    text-align: center;
  }

  .search-container {
    margin-right: 0;
    margin-top: 10px;
  }
}

</style>