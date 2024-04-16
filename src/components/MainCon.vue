<template>
  <div class="con pb-28">
    <div class="max-w-6xl mx-auto">
      <TheNav class="mb-28" />
      <div
        class="flex flex-col lg:flex-row items-center justify-between space-y-12 lg:space-y-0"
      >
        <div class="max-w-xl flex flex-col items-start text-left space-y-12">
          <span class="primary-color"> Фраза для привлечения внимания </span>
          <span class="text-white second-text">
            Описание продукта Описание продукта Описание продукта Описание
            продукта Описание продукта Описание продукта Описание продукта
            Описание продукта Описание продукта Описание продукта Описание
          </span>
          <div class="flex items-center space-x-4">
            <button class="buyButton rounded-xl px-2 py-4">
              КУПИТЬ СЕЙЧАС
            </button>
            <span class="underline text-white font-bold">
              Посмотреть продукт
            </span>
          </div>
        </div>
        <img src="../assets/mainConImg.svg" alt="" />
      </div>
    </div>
    <div class="callButton" @click="handleClick">
      <img src="../assets/callIcon.svg" alt="" />
    </div>
  </div>

  <request-modal ref="requestmodal">
    <template v-slot:header>
      <h3 class="mainText">Бесплатный звонок</h3>
    </template>
    <template v-slot:body>
      <p class="secondText text-center">
        Наш специалист свяжется с вами в течение одной минуты
      </p>
      <input type="text" class="styledInput" placeholder="Name" />
      <input type="text" class="styledInput" placeholder="+7 (000) 000 00 00" />
    </template>
  </request-modal>
</template>

<script>
import TheNav from "./TheNav.vue";
import RequestModal from "./RequestModal.vue";

export default {
  data() {
    return {};
  },
  components: {
    TheNav,
    RequestModal,
  },
  methods: {
    handleClick() {
      this.$refs.requestmodal.openModal();
    },
  },
};
</script>

<style scoped>
.styledInput {
  font-family: Inter;
  font-size: 25px;
  font-weight: 400;
  line-height: 27.84px;
  text-align: left;
  border-bottom: 1px solid #0000003b;
  padding: 0.5rem;
}
.callButton {
  border-radius: 100000px;
  background: #e3b253;
  position: fixed;
  right: 2rem;
  bottom: 2rem;
  padding: 10px;
}
.callButton img {
  width: 40px;
}
.buyButton {
  background: #d9d9d9;
  font-family: Inter;
  font-size: 15px;
  font-weight: 800;
  text-align: left;
}
.con {
  background: #656565;
}

.primary-color {
  font-family: Ovo;
  font-size: 100px;
  font-weight: 400;
  line-height: 120px;
  text-align: left;
}

.second-text {
  font-family: Inter;
  font-size: 20px;
  font-weight: 500;
  line-height: 30px;
}
</style>
