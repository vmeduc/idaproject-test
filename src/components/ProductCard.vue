<template>
  <div class="product-card">
    <div class="product-card__image">
      <img :src="product.image" alt="Product" />
    </div>
    <div class="product-card__main">
      <h3 class="product-card__title">{{product.name}}</h3>
      <div class="product-card__text">{{product.text}}</div>
    </div>
    <h2 class="product-card__price">{{product.price}}</h2>
  </div>
</template>

<script>
export default {
  props: {
    product: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style scoped>
.product-card {
  width: 332px;
  height: 423px;
  background-color: #fffefb;
  color: #3F3F3F;
  overflow: hidden;
  box-shadow: 0px 20px 30px rgba(0, 0, 0, 0.04),
    0px 6px 10px rgba(0, 0, 0, 0.02);
  border-radius: 4px;
}

.product-card__image {
  width: 332px;
  height: 200px;
}

.product-card__image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.product-card__main {
  display: flex;
  flex-direction: column;
  gap: 16px;
  padding: 16px 16px 32px 16px;
}

.product-card__title {
  font-weight: 600;
  font-size: 20px;
  line-height: 25px;
}

.product-card__text {
  font-weight: 400;
  font-size: 16px;
  line-height: 20px;
  width: 300px;
  height: 80px;
  overflow: auto;
}

.product-card__price {
  margin: auto auto 24px 16px;
  font-weight: 600;
  font-size: 24px;
  line-height: 30px;
}
</style>