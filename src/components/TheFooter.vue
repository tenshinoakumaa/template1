<template>
  <div class="con py-28">
    <div
      class="max-w-6xl mx-auto flex lg:flex-row lg:justify-between flex-col items-center lg:items-start space-y-14 lg:space-y-0"
    >
      <div class="div space-y-4">
        <span class="mainText">Меню сайта</span>
        <ul class="text-white flex flex-col items-start space-y-4">
          <li>О продукте</li>
          <li>Тех характеристики</li>
          <li>Каталог</li>
          <li>Контакты</li>
          <li>Корзина</li>
        </ul>
      </div>

      <div class="div space-y-4">
        <span class="mainText">Контакты</span>
        <ul class="text-white flex flex-col items-start space-y-4">
          <li>Адрес</li>
          <li>Номер</li>
          <li>Почта</li>
        </ul>
      </div>

      <div class="div flex flex-row space-x-4 items-start">
        <img src="../assets/telegramIcon.svg" alt="" />
        <img src="../assets/instagramIcon.svg" alt="" />
        <img src="../assets/whatsappIcon.svg" alt="" />
      </div>
    </div>
  </div>
</template>

<style scoped>
.con {
  background: #474646e0;
}
img {
  width: 30px;
}
.mainText {
  font-family: Inter;
  font-size: 38px;
  font-weight: 500;
  line-height: 45.99px;
  text-align: left;
  color: #e3b253;
}

ul {
  list-style: inside;
}

@media (max-width: 1024px) {
  .div {
    max-width: 15rem;
    width: 100%;
  }
}
</style>
