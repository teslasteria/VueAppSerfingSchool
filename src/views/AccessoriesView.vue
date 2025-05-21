<template>
    <h1 class="main-title">Accessories</h1>

<!-- Navigation -->
<NavBar />

<!-- Main Content -->
<main class="accessories-container">
  <section class="accessories-intro">
    <h2>Essential Gear for Every Surfer</h2>
    <p>
      At Shell Surfing School, we offer only the highest quality accessories
      to enhance your surfing experience. All products come with our quality
      guarantee.
    </p>
  </section>

  <div class="accessories-grid">
    <!-- Wetsuit -->
    <article class="accessory-card">
      <div class="card-image">
        <img src="@/assets/img/wetsuit.jpg" alt="Premium Wetsuit" loading="lazy" />
      </div>
      <div class="card-content">
        <h3>NeoFlex Wetsuits</h3>
        <p class="price">$149.99 - $299.99</p>
        <p>
          Stay warm and flexible in all conditions with our premium
          wetsuits. Available in various thicknesses for different water
          temperatures.
        </p>
        <ul class="features">
          <li>100% Neoprene</li>
          <li>Flatlock stitching</li>
          <li>UV protection</li>
        </ul>
        <button class="btn-add-to-cart">Add to Cart</button>
      </div>
    </article>

    <!-- Leash -->
    <article class="accessory-card">
      <div class="card-image">
        <img src="@/assets/img/leash.jpg" alt="Surfboard Leash" loading="lazy" />
      </div>
      <div class="card-content">
        <h3>ProLine Leashes</h3>
        <p class="price">$39.99 - $69.99</p>
        <p>
          High-performance leashes that keep you connected to your board in
          all conditions.
        </p>
        <ul class="features">
          <li>Swivel cuff prevents tangling</li>
          <li>Durable polyurethane cord</li>
          <li>Multiple lengths available</li>
        </ul>
        <button class="btn-add-to-cart">Add to Cart</button>
      </div>
    </article>

    <!-- Wax -->
    <article class="accessory-card">
      <div class="card-image">
        <img src="@/assets/img/wax.jpg" alt="Surf Wax" loading="lazy" />
      </div>
      <div class="card-content">
        <h3>OceanGrip Wax</h3>
        <p class="price">$4.99 - $9.99</p>
        <p>
          Premium surf wax for maximum traction in any water temperature.
        </p>
        <ul class="features">
          <li>All-natural formula</li>
          <li>Temperature-specific variants</li>
          <li>Long-lasting grip</li>
        </ul>
        <button class="btn-add-to-cart">Add to Cart</button>
      </div>
    </article>

    <!-- Bag -->
    <article class="accessory-card">
      <div class="card-image">
        <img src="@/assets/img/bag.jpg" alt="Surfboard Bag" loading="lazy" />
      </div>
      <div class="card-content">
        <h3>BoardGuard Bags</h3>
        <p class="price">$89.99 - $159.99</p>
        <p>
          Protect your board with our durable and lightweight surfboard
          bags.
        </p>
        <ul class="features">
          <li>Padded protection</li>
          <li>Water-resistant material</li>
          <li>Multiple size options</li>
        </ul>
        <button class="btn-add-to-cart">Add to Cart</button>
      </div>
    </article>
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
@import '@/assets/css/accessories.css';
@import '@/assets/css/style.css';
</style>