<script> 
import { ref, reactive } from 'vue'
import NavBar from '@/components/NavBar.vue'
import AppFooter from '@/components/AppFooter.vue'
export default {
  name: 'VueAppView',
  components: {
    NavBar,
    AppFooter,
    setup() {
        const message = ref('Hello Vue!')
        const imageSrc = ref(require('@/assets/img/Colorful Surfboards at a Tropical Beach.jpeg'))
        const isActive = ref(true)
        const hasError = ref(false)
            
        // Массив продуктов
        const products = reactive([
            {
                id: 1,
                name: 'Pro Surfboard',
                price: 599.99,
                description: 'High-performance surfboard for experienced surfers',
                image: require('@/assets/img/Colorful Surfboards at a Tropical Beach.jpeg')
            },
            {
                id: 2,
                name: 'Beginner Surfboard',
                price: 299.99,
                description: 'Stable and easy to use for beginners',
                image: require('@/assets/img/Sunny Beach Serenity.jpeg')
            },
            {
                id: 3,
                name: 'Wetsuit',
                price: 149.99,
                description: '3mm neoprene wetsuit for warm waters',
                image: require('@/assets/img/wetsuit.jpg')
            },
            {
                id: 4,
                name: 'Surfboard Leash',
                price: 39.99,
                description: 'Keeps your board close when you fall',
                image: require('@/assets/img/leash.jpg')
            },
            {
                id: 5,
                name: 'Surf Wax',
                price: 9.99,
                description: 'Provides grip for your feet on the board',
                image: require('@/assets/img/wax.jpg')
            },
            {
                id: 6,
                name: 'Surfboard Bag',
                price: 89.99,
                description: 'Protects your board during transport',
                image: require('@/assets/img/bag.jpg')
            },
            {
                id: 7,
                name: 'Rash Guard',
                price: 29.99,
                description: 'Protects from sun and rash',
                image: require('@/assets/img/t-shirt.jpg')
            },
            {
                id: 8,
                name: 'Surf Hat',
                price: 24.99,
                description: 'Keeps the sun out of your eyes',
                image: require('@/assets/img/mug.jpg')
            },
            {
                id: 9,
                name: 'Surf Sunglasses',
                price: 59.99,
                description: 'Polarized lenses for better visibility',
                image: require('@/assets/img/sticker.jpg')
            },
            {
                id: 10,
                name: 'Surf Watch',
                price: 199.99,
                description: 'Tracks tides and surf conditions',
                image: require('@/assets/img/Stylish Surf Shop Interior.jpeg')
            }
        ])
            
        // Корзина
        const cart = reactive([])

        // Новостные рассылки
        const newsletters = reactive([
        { id: 1, name: 'Monthly Surf Reports' },
        { id: 2, name: 'Special Offers' },
        { id: 3, name: 'Surfing Tips' },
        { id: 4, name: 'Event Invitations' }
        ])

    
        }
    }
}
</script>

<template>
    <div id="app">

<!-- navigation -->
<NavBar />

<h1 class="main-title" id="header1">Vue.js Application</h1>
<main class="vue-container">
    
    <!-- 2. various type of binding -->
    <section class="binding-section">
        <h2>Data Binding Examples</h2>
        
        <div class="binding-example">
            <h3>Text Binding (v-model)</h3>
            <input v-model="message" placeholder="Type something">
            <p>You typed: {{ message }}</p>
        </div>
        
        <div class="binding-example">
            <h3>Attribute Binding (v-bind)</h3>
            <img v-bind:src="imageSrc" alt="Surfing image" style="max-width: 300px;">
            <input type="text" v-model="imageSrc" placeholder="Change image URL">
        </div>
        
        <div class="binding-example">
            <h3>Class Binding (v-bind:class)</h3>
            <div v-bind:class="{ 'active': isActive, 'error': hasError }">
                This div's class changes dynamically
            </div>
            <button @click="toggleClass">Toggle Class</button>
        </div>
    </section>
    
    <!-- 3. array's output -->
    <section class="array-section">
        <h2>Surfing Products ({{ products.length }} items)</h2>
        <div class="product-grid">
            <div v-for="(product, index) in products" :key="index" class="product-card">
                <img :src="product.image" :alt="product.name" loading="lazy">
                <h3>{{ product.name }}</h3>
                <p class="price">${{ product.price }}</p>
                <p>{{ product.description }}</p>
                <button @click="addToCart(product)">Add to Cart</button>
            </div>
        </div>
    </section>
    
    <!-- 4. conditional rendering -->
    <section class="conditional-section">
        <h2>Cart ({{ cart.length }} items)</h2>
        <button @click="showCart = !showCart">
            {{ showCart ? 'Hide Cart' : 'Show Cart' }}
        </button>
        
        <div v-if="showCart">
            <div v-if="cart.length > 0">
                <table>
                    <thead>
                        <tr>
                            <th>Product</th>
                            <th>Price</th>
                            <th>Quantity</th>
                            <th>Action</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr v-for="(item, index) in cart" :key="index">
                            <td>{{ item.name }}</td>
                            <td>${{ item.price }}</td>
                            <td>{{ item.quantity }}</td>
                            <td><button @click="removeFromCart(index)">Remove</button></td>
                        </tr>
                    </tbody>
                    <tfoot>
                        <tr>
                            <td colspan="4">Total: ${{ cartTotal }}</td>
                        </tr>
                    </tfoot>
                </table>
            </div>
            <div v-else>
                <p>Your cart is empty</p>
            </div>
        </div>
    </section>
    
    <!-- 5. event handler -->
    <section class="event-section">
        <h2>Newsletter Signup</h2>
        <form @submit.prevent="submitForm">
            <div class="form-group">
                <label>Email:</label>
                <input type="email" v-model="email" required placeholder="Your email">
            </div>
            <div class="form-group">
                <label>Subscribe to:</label>
                <select v-model="selectedNewsletters" multiple>
                    <option v-for="newsletter in newsletters" :key="newsletter.id" :value="newsletter.id">
                        {{ newsletter.name }}
                    </option>
                </select>
            </div>
            <button type="submit">Subscribe</button>
        </form>
        <div v-if="submitted" class="success-message">
            Thank you for subscribing! You'll receive updates on:
            <ul>
                <li v-for="id in selectedNewsletters" :key="id">
                    {{ getNewsletterName(id) }}
                </li>
            </ul>
        </div>
    </section>
</main>
</div>

<AppFooter />
</template>

<style scoped>
@import '@/assets/css/vue-app.css';
@import '@/assets/css/style.css';
</style>