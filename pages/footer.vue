<template>
    <footer class="footer bg-light pt-5">
      <div class="container">
        <div class="row">

          <div class="col-md-12 text-center mb-4">
            <p><i class="bi bi-whatsapp"></i> Whatsapp Destek &nbsp; | &nbsp; <i class="bi bi-telephone"></i> 0850 288 62 84 &nbsp; | &nbsp; <i class="bi bi-clock"></i> Çalışma saatleri: 08:00 - 00:00 &nbsp; | &nbsp; <i class="bi bi-envelope"></i> bilgi@mavi.com</p>
          </div>
        </div>
  
        <hr />
  
        <div class="row">
          <div class="col-md-3">
            <h5>APP'İ İNDİR</h5>
            <div class="d-flex mb-3">
              <img src="/images/image_google_ply.png" alt="Google Play" class="me-2" width="100" />
              <img src="/images/image_app_store.png" alt="App Store" class="me-2" width="100" />
              <img src="/images/image_app_gallery.png" alt="App Gallery" width="100" />
            </div>
            <div class="d-flex social-icons">
              <i class="bi bi-instagram me-3"></i>
              <i class="bi bi-x me-3"></i>
              <i class="bi bi-facebook me-3"></i>
              <i class="bi bi-spotify me-3"></i>
              <i class="bi bi-youtube me-3"></i>
              <i class="bi bi-tiktok"></i>
            </div>
            <div class="mt-3">
              <p>Türkçe <i class="bi bi-caret-down-fill"></i></p>
            </div>
            <div class="mt-3">
              <img src="/images/image_kod.png" alt="ETBIS" width="100" />
              <p class="small">ETBİS'e Kayıtlıdır.</p>
            </div>
          </div>
  
          <div class="col-md-3">
            <h5>YARDIM</h5>
            <ul class="list-unstyled">
              <li><a href="/order-tracking">Sipariş Sorgulama</a></li>
              <li><a href="/returns-exchanges">İade ve Değişim</a></li>
              <li><a href="/faq">Sıkça Sorulan Sorular</a></li>
              <li><a href="/size-chart">Beden Tablosu</a></li>
              <li><a href="/operation-guide">İşlem Rehberi</a></li>
              <li><a href="/site-map">Site Haritası</a></li>
              <li><a href="/nearest-store">En Yakın Mavi</a></li>
              <li><a href="/contact-us">Bize Ulaşın</a></li>
              <li><a href="/inclusive-communication">Kapsayıcı İletişim</a></li>
            </ul>
          </div>
  
          <div class="col-md-3">
            <h5>KURUMSAL BİLGİLER</h5>
            <ul class="list-unstyled">
              <li><a href="/corporate-website">Kurumsal Web Sitesi</a></li>
              <li><a href="/about-us">Hakkımızda</a></li>
              <li><a href="/sustainability">Sürdürülebilirlik</a></li>
              <li><a href="/investor-relations">Yatırımcı İlişkileri</a></li>
              <li><a href="/career">Kariyer</a></li>
              <li><a href="/principles">Mavi’de Biz ve İlkelerimiz</a></li>
              <li><a href="/information-society-services">Bilgi Toplumu Hizmetleri</a></li>
              <li><a href="/corporate-sales">Kurumsal Satış</a></li>
              <li><a href="/franchise-application">Bayilik Başvuru Formu</a></li>
              <li><a href="/contact">İletişim</a></li>
            </ul>
          </div>
  
          
          <div class="col-md-3">
            <h5>FAVORİ KATEGORİLER</h5>
            <ul class="list-unstyled">
              <li><a href="/women-sweaters">Kadın Triko Kazak</a></li>
              <li><a href="/women-jackets">Kadın Şişme Mont</a></li>
              <li><a href="/women-outerwear">Kadın Dış Giyim</a></li>
              <li><a href="/women-denim-jackets">Kadın Denim Ceket</a></li>
              <li><a href="/women-coats">Kadın Ceket</a></li>
              <li><a href="/women-scarves">Kadın Şal & Atkı</a></li>
              <li><a href="/women-sweatshirts">Kadın Sweatshirt</a></li>
              <li><a href="/women-jeans">Kadın Jean</a></li>
              <li><a href="/women-trousers">Kadın Pantolon</a></li>
              <li><a href="/women-corduroy-pants">Kadın Kadife Pantolon</a></li>
              <li><a href="/women-shirts">Kadın Gömlek</a></li>
              <li><a href="/women-joggers">Kadın Eşofman Altı</a></li>
            </ul>
          </div>
        </div>
  
        <hr />
  
        <!-- Footer Bottom Links -->
        <div class="row">
          <div class="col text-center">
            <p>© 2024 Mavi - Tüm Hakları Saklıdır</p>
            <div class="footer-links">
              <a href="#">Mavi Üyelik Sözleşmesi</a> |
              <a href="#">Kartuş Üyelik Sözleşmesi</a> |
              <a href="#">Aydınlatma Metinleri</a> |
              <a href="#">Çerez Aydınlatma Metni</a>
            </div>
          </div>
        </div>
      </div>
    </footer>
  </template>
  
  <script>
  export default {
    name: "Footer",
  };
  </script>
  
  <style scoped>
  .footer {
    font-size: 14px;
  }
  .footer a {
    color: #6c757d; 
    text-decoration: none;
  }
  .footer a:hover {
    text-decoration: underline;
  }
  .social-icons i {
    font-size: 20px;
  }
  .footer-links a {
    color: #6c757d; 
    margin: 0 10px;
  }
  .footer-links a:hover {
    text-decoration: underline;
  }
  </style>
  