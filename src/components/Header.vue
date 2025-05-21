<template>
    <header class="header">
      <div class="container header__container">
        <a href="/" class="logo">
          <img src="@/assets/img/sea-wave-clipart-lg.png" alt="Логотип" class="logo__img">
        </a>
        
        <nav class="nav">
          <ul class="nav__list">
            <li class="nav__item" v-for="link in links" :key="link.path">
              <router-link :to="link.path" class="nav__link">{{ link.title }}</router-link>
            </li>
          </ul>
        </nav>
        
        <button class="burger" @click="toggleMenu" aria-label="Меню">
          <span class="burger__line"></span>
        </button>
      </div>
    </header>
  </template>
  
  <script>
  export default {
    data() {
      return {
        links: [
          { path: '/', title: 'Главная' },
          { path: '/about', title: 'О нас' },
          { path: '/services', title: 'Услуги' },
          { path: '/portfolio', title: 'Портфолио' },
          { path: '/contacts', title: 'Контакты' }
        ],
        isMenuOpen: false
      }
    },
    methods: {
      toggleMenu() {
        this.isMenuOpen = !this.isMenuOpen
        document.body.classList.toggle('no-scroll', this.isMenuOpen)
      }
    }
  }
  </script>
  
  <style lang="scss" scoped>
  .header {
    background-color: #fff;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
    position: fixed;
    width: 100%;
    top: 0;
    left: 0;
    z-index: 100;
  }
  
  .nav__list {
    display: flex;
    align-items: center;
    gap: 40px;
  }
  
  .nav__link {
    color: #333;
    font-weight: 500;
    transition: color 0.3s ease;
    
    &:hover {
      color: #4a76a8;
    }
    
    &.router-link-exact-active {
      color: #4a76a8;
      position: relative;
      
      &::after {
        content: '';
        position: absolute;
        bottom: -5px;
        left: 0;
        width: 100%;
        height: 2px;
        background-color: #4a76a8;
      }
    }
  }
  
  .burger {
    display: none;
    /* ... остальные стили бургера ... */
  }
  
  @media (max-width: 768px) {
    /* ... мобильные стили ... */
  }
  </style>