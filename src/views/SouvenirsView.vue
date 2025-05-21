<template>
    <h1 class="main-title">Souvenirs</h1>

<!-- Navigation -->
<NavBar />

<!-- Main Content -->
<main class="souvenirs-container">
  <h2 class="section-title">Our Souvenir Collection</h2>
  <p class="section-intro">
    Bring home a memory from your surfing adventure with our high-quality
    branded merchandise.
  </p>

  <div class="souvenirs-grid">
    <!-- T-Shirt -->
    <div class="souvenir-card">
      <div class="souvenir-image">
        <img
          src="img/t-shirt.jpg"
          alt="Shell Surfing T-Shirt"
          loading="lazy"
        />
      </div>
      <div class="souvenir-info">
        <h3>Surf Culture T-Shirts</h3>
        <p class="price">$24.99</p>
        <p>
          100% cotton t-shirts with our unique surf designs. Available in
          multiple colors and sizes.
        </p>
        <button class="btn-buy">Add to Cart</button>
      </div>
    </div>

    <!-- Mug -->
    <div class="souvenir-card">
      <div class="souvenir-image">
        <img src="img/mug.jpg" alt="Shell Surfing Mug" loading="lazy" />
      </div>
      <div class="souvenir-info">
        <h3>Ceramic Mugs</h3>
        <p class="price">$14.99</p>
        <p>
          High-quality ceramic mugs featuring our logo. Dishwasher and
          microwave safe.
        </p>
        <button class="btn-buy">Add to Cart</button>
      </div>
    </div>

    <!-- Sticker -->
    <div class="souvenir-card">
      <div class="souvenir-image">
        <img
          src="img/sticker.jpg"
          alt="Shell Surfing Sticker"
          loading="lazy"
        />
      </div>
      <div class="souvenir-info">
        <h3>Vinyl Stickers</h3>
        <p class="price">$3.99</p>
        <p>
          Waterproof vinyl stickers perfect for laptops, boards or water
          bottles.
        </p>
        <button class="btn-buy">Add to Cart</button>
      </div>
    </div>
  </div>
</main>
<AppFooter />
</template>

<script>
import NavBar from '@/components/NavBar.vue'
import AppFooter from '@/components/AppFooter.vue'
export default {
  name: 'AboutView',
  components: {
    NavBar,
    AppFooter
  }
}
</script>

<style scoped>
@import '@/assets/css/souvenirs.css';
@import '@/assets/css/style.css';
</style>