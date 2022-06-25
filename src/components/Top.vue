<template>
  <div class="top">
    <h1 class="top__title">Добавление товара</h1>
    <select class="top__filter-selector">
      <option value="default">По умолчанию</option>
      <option value="price">По цене</option>
      <option value="name">По имени</option>
    </select>
  </div>
</template>

<script>
export default {

}
</script>

<style>
.top {
  display: flex;
  justify-content: space-between;
}

.top__title {
  font-style: normal;
  font-weight: 600;
  font-size: 28px;
  line-height: 35px;
  color: #3F3F3F;
}

.top__filter-selector {
  font-family: 'Source Sans Pro';
  font-style: normal;
  font-weight: 400;
  width: 121.49px;
  height: 36px;
  background: #FFFEFB;
  box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
  border-radius: 4px; 
  border: none;
  font-size: 12px;
  line-height: 15px;
  color: #B4B4B4;
  padding-left: 16px;
}

.top__filter-selector:focus {
  outline: 1px solid lightgray;
}
</style>