<template>
  <div id="app">
    <Top />
    <div class="main">
      <div class="sidebar">
        <ProductForm />
      </div>
      <div class="grid">
        <ProductCard v-for="p in productList" :product="p" :key="p.id" />
      </div>
    </div>
  </div>
</template>

<script>
import Top from "@/components/Top.vue";
import ProductForm from "@/components/ProductForm.vue";
import ProductCard from "@/components/ProductCard.vue";

export default {
  components: {
    Top,
    ProductForm,
    ProductCard,
  },
  data() {
    return {
      productList: [
        {
          id: 1,
          name: "iPhone 5",
          price: "10 000 руб.",
          image: "https://zor.uz/pics/oi/2020/09/5417585_m.jpg",
          text: "iPhone 5 — смартфон компании Apple, представляет шестое поколение iPhone.",
        },
        {
          id: 2,
          name: "iPhone 5",
          price: "10 000 руб.",
          image: "https://zor.uz/pics/oi/2020/09/5417585_m.jpg",
          text: "iPhone 5 — смартфон компании Apple, представляет шестое поколение iPhone.",
        },
        {
          id: 3,
          name: "iPhone 5",
          price: "10 000 руб.",
          image: "https://zor.uz/pics/oi/2020/09/5417585_m.jpg",
          text: "iPhone 5 — смартфон компании Apple, представляет шестое поколение iPhone.",
        },
      ],
      currentId: 1,
    };
  },
  
};
</script>

<style>
#app {
  margin: 32px;
}

.main {
  display: flex;
  gap: 16px;
  margin-top: 16px;
}

.grid {
  display: grid;
  grid-template: "a b c";
  gap: 16px;
}
@media (max-width: 1439px) {
  .grid {
    grid-template: "a b";
  }
}

/* mixins */

.product-form,
.product-card {
  box-shadow: 0px 20px 30px rgba(0, 0, 0, 0.04),
    0px 6px 10px rgba(0, 0, 0, 0.02);
  border-radius: 4px;
}
</style>