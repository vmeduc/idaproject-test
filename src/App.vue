<template>
  <div id="app">
    <Top />
    <div class="main">
      <div class="sidebar">
        <ProductForm @addProduct="onAddProduct" />
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
          id: 0,
          name: "iPhone 5",
          price: "10 000 руб.",
          image: "https://vseotzyvy.ru/media/review_images/1601750765.jpg",
          text: "iPhone 5 — смартфон компании Apple, представляет шестое поколение iPhone.",
        },
      ],
      currentId: 0,
    };
  },
  methods: {
    onAddProduct(product) {
      if (this.validate(product)) {
        product.id = this.nextId();
        this.productList.push(product);
        this.$nextTick(() => window.scrollTo(0, document.body.scrollHeight));
      } else {
        alert("Не все обязательные поля заполнены")
      }
    },
    nextId() {
      return ++this.currentId;
    },
    validate(product) {
      return (product.name && product.price && product.image)
    }
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
@media (max-width: 760px) {
  .main {
    flex-direction: column;
  }
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
@media (max-width: 1090px) {
  .grid {
    grid-template: "a";
  }
}
</style>