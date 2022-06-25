<template>
  <form class="product-form">
    <div class="product-form__main">
      <div class="product-form__line">
        <label class="product-form__label" for="product-name">
          Наименование товара
          <div class="required-sign"></div>
        </label>
        <input
          class="product-form__input"
          type="text"
          id="product-name"
          placeholder="Введите наименование товара"
          required
        />
      </div>
      <div class="product-form__line">
        <label class="product-form__label" for="product-description">
          Описание товара
        </label>
        <textarea
          class="product-form__textarea"
          type="text"
          id="product-description"
          placeholder="Введите описание товара"
        ></textarea>
      </div>
      <div class="product-form__line">
        <label class="product-form__label" for="product-image-link">
          Ссылка на изображение товара
          <div class="required-sign"></div>
        </label>
        <input
          class="product-form__input"
          type="text"
          id="product-image-link"
          placeholder="Введите ссылку"
          required
        />
      </div>
      <div class="product-form__line">
        <label class="product-form__label" for="product-price">
          Цена товара
          <div class="required-sign"></div>
        </label>
        <input
          class="product-form__input"
          type="text"
          id="product-price"
          placeholder="Введите цену"
          required
        />
      </div>
    </div>
    <div class="product-form__actions">
      <button class="product-form__button" type="submit">Добавить товар</button>
    </div>
  </form>
</template>

<script>
export default {

};
</script>

<style>
.product-form {
  display: flex;
  flex-direction: column;
  gap: 24px;
  padding: 24px;
  width: 332px;
  height: 440px;
  background-color: #fffefb;
  position: sticky;
  top: 24px;
}

.product-form__main {
  display: flex;
  flex-direction: column;
  gap: 16px;
}

.product-form__line {
  display: flex;
  flex-direction: column;
  gap: 4px;
}

.product-form__label,
.product-form__input,
.product-form__textarea {
  font-family: 'Source Sans Pro';
  font-style: normal;
  font-weight: 400;
}

.product-form__button,
.product-form__input,
.product-form__textarea {
  display: block;
}

.product-form__input, .product-form__button {
  width: 284px;
  height: 36px;
}

.product-form__textarea {
  width: 284px;
  height: 108px;
}

.product-form__input, .product-form__textarea {
  border: none;
  background: #FFFEFB;
  box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
  border-radius: 4px;
  font-size: 12px;
  line-height: 15px;
  padding-left: 16px;
}

.product-form__label {
  position: relative;
  width: fit-content;
  font-size: 10px;
  line-height: 13px;
  letter-spacing: -0.02em;
}

.product-form__textarea {
  resize: none;
  padding-top: 10px;
}

.product-form__button {
  border: none;
  border-radius: 10px;
  background: #EEEEEE;
  text-align: center;
  font-family: 'Inter';
  font-style: normal;
  font-weight: 600;
  font-size: 12px;
  line-height: 15px;
  letter-spacing: -0.02em;
  color: #B4B4B4;
}

.product-form__input:focus, 
.product-form__textarea:focus, 
.product-form__button:focus {
  outline: 1px solid lightgray;
}

.product-form__input::placeholder, 
.product-form__textarea::placeholder {
  color: #B4B4B4;
}

.required-sign {
  width: 4px;
  height: 4px;
  background-color: #FF8484;
  border-radius: 4px;
  position: absolute;
  top: 0;
  left: calc(100% + 1px);
}
</style>