<template>
  <div id="CheckBox">
    <h1>Выберите категории товаров</h1>
    <div>
      <label>
        <input type="checkbox" value="Chairs" v-model="selectedCategories">
        Chairs
      </label>
      <label>
        <input type="checkbox" value="Beds" v-model="selectedCategories">
        Beds
      </label>
      <label>
        <input type="checkbox" value="Sofa" v-model="selectedCategories">
        Sofa
      </label>
    </div>
    <div v-if="selectedCategories.includes('Chairs')">
      <h2>Товары Категории 1</h2>
      <ul>
        <li><img src="" alt=""></li>
        <li><img src="" alt=""></li>
        <li><img src="" alt=""></li>
      </ul>
    </div>
    <div v-if="selectedCategories.includes('Beds')">
      <h2>Товары Категории 2</h2>
      <ul>
        <li>Продукт 2.1</li>
        <li>Продукт 2.2</li>
        <li>Продукт 2.3</li>
      </ul>
    </div>
    <div v-if="selectedCategories.includes('Sofa')">
      <h2>Товары Категории 3</h2>
      <ul>
        <li>Продукт 3.1</li>
        <li>Продукт 3.2</li>
        <li>Продукт 3.3</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      selectedCategories: []
    }
  }
}
</script>

<style>

</style>
