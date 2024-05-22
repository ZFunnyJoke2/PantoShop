<script>
export default {
  name: 'TheHeader',
  data() {
    return {
      showDropdown: false
    };
  },
  methods: {
    toggleDropdown() {
      this.showDropdown = !this.showDropdown;
    },
    handleClickOutside(event) {
      const header = this.$el;
      if (!header.contains(event.target)) {
        this.showDropdown = false;
      }
    }
  },
  mounted() {
    document.addEventListener('click', this.handleClickOutside);
  },
  beforeUnmount() {
    document.removeEventListener('click', this.handleClickOutside);
  }
}
</script>

<template>
  <header class="header">
    <div class="container">
      <h1 class="logo">Panto</h1>
      <nav class="nav">
        <ul>
          <li @click.stop="toggleDropdown">
            <a href="#" class="dropdown-link">Furniture</a>
            <span :class="{'arrow': true, 'open': showDropdown}" class="dropdown-container"></span>
            <ul v-if="showDropdown" class="dropdown">
              <li><a href="#">Chair</a></li>
              <li><a href="#">Beds</a></li>
              <li><a href="#">Sofa</a></li>
            </ul>
          </li>
          <li><a href="#">Shop</a></li>
          <li><a href="#">About us</a></li>
          <li><a href="#">Contact</a></li>
        </ul>
      </nav>
      <div class="cart">
        <img src="../assets/img/Bag.png" alt="Bag"/>
      </div>
    </div>
  </header>

</template>

<style>
  *{
    font-family: Gilroy-Light, sans-serif;
  }
  .header {
    background-color: #333;
    color: #fff;
    padding: 1rem 0;
  }
  .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 1rem;
  }
  .logo {
    font-size: 1.5rem;
  }
  .nav ul {
    list-style: none;
    display: flex;
    margin: 0;
    padding: 0;
  }
  .nav li {
    position: relative;
    margin-left: 1rem;
  }
  .nav a {
    color: #fff;
    text-decoration: none;
  }
  .nav a:hover {
    text-decoration: underline;
  }
  .dropdown-container {
    display: flex;
    align-items: center;
  }
  .dropdown-link {
    display: inline-flex;
    align-items: center;
    flex-direction: column;
  }
  .arrow {
    margin-left: 0.5rem;
    width: 0;
    height: 0;
    border-left: 5px solid transparent;
    border-right: 5px solid transparent;
    border-top: 5px solid #fff;
    transition: transform 0.3s ease;
  }
  .arrow.open {
    transform: rotate(180deg);
  }
  .dropdown {
    position: absolute;
    top: 100%;
    left: 0;
    background-color: #444;
    list-style: none;
    margin: 0;
    padding: 0.5rem 0;
    display: block;
  }
  .dropdown li {
    margin: 0;
  }
  .dropdown a {
    padding: 0.5rem 1rem;
    display: block;
    white-space: nowrap;
  }
  .dropdown a:hover {
    background-color: #555;
  }
  </style>