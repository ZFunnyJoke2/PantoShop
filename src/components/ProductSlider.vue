<template>
  <div class="slider-title">
    <h2>Best selling product</h2>
  </div>
    <div class="slider">
      <button class="arrow left" @click="prevSlide">&#9664;</button>
      <div class="slider-wrapper" :style="sliderStyle">
        <div class="slide" v-for="(product, index) in products" :key="index">
          <img :src="product.image" :alt="product.name" class="product-image"/>
          <div class="product-info">
            <h3>{{ product.name }}</h3>
            <p>{{ product.price }}</p>
          </div>
        </div>
      </div>
      <button class="arrow right" @click="nextSlide">&#9654;</button>
    </div>
</template>

<script>
export default {
  data() {
    return {
      currentIndex: 0,
      products: [
        { image: '@/assets/img/1chair.jpg', name: 'Sakarias Armchair', price: '$392' },
        { image: '@/assets/img/2chair.jpg', name: 'Baltasar Chair', price: '$299' },
        { image: '@/assets/img/3chair.jpg', name: 'Anjay Chair', price: '$519' },
        { image: '@/assets/img/4chair.jpg', name: 'Nyantuy Chair', price: '$921' }
      ]
    };
  },
  computed: {
    sliderStyle() {
      return {
        transform: `translateX(-${this.currentIndex * 100}%)`
      };
    }
  },
  methods: {
    prevSlide() {
      this.currentIndex = (this.currentIndex > 0) ? this.currentIndex - 1 : this.products.length - 1;
    },
    nextSlide() {
      this.currentIndex = (this.currentIndex < this.products.length - 1) ? this.currentIndex + 1 : 0;
    }
  }
};
</script>

<style>
.slider-title{
  display: flex;
  justify-content: center;
  font-size: 30px;
}
.slider {
  margin-top: 10rem;
  position: relative;
  width: 100%;
  overflow: hidden;
  display: flex;
  align-items: center;
  background: #fff;
  border: 3px solid #333;
  border-radius: 10px;
}

.slider-wrapper {
  display: flex;
  transition: transform 0.5s ease-in-out;
}

.slide {
  min-width: calc(100% / 1.37); /* Отрегулируйте это значение в зависимости от количества видимых слайдов */
  box-sizing: border-box;
  padding: 10px; /* Уменьшите отступы */
  text-align: center;
}

.product-image {
  width: 100px;
  height: auto;
}

.arrow {
  background: none;
  border: none;
  font-size: 2em;
  cursor: pointer;
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
}

.left {
  left: 10px;
}

.right {
  right: 10px;
}
</style>