<template>
  <div class="con py-28 flex lg:block">
    <div class="max-w-6xl mx-auto flex justify-between items-center">
      <div class="flex flex-col items-start lg:items-start lg:w-1/2 space-y-8">
        <span class="mainText text-left">Имя и фамилия</span>
        <input type="text" placeholder="Emma Watson" />
        <span class="mainText text-left">Номер телефона</span>
        <input type="text" placeholder="+77020590617" />
        <div class="flex items-center space-x-4">
          <input type="checkbox" class="checkbox" />
          <span class="text">
            Дайте мне знать о скидках, распродажах и новых акциях
          </span>
        </div>
      </div>
      <img src="../assets/secondConImg.svg" alt="" class="nonVis lg:visible" />
    </div>
  </div>

  <success-modal ref="successmodal">
    <template v-slot:header>
      <h3 class="mainText">Поздравления</h3>
    </template>
    <template v-slot:body>
      <p class="secondText text-center">{{ successMessage }}</p>
    </template>
  </success-modal>
</template>

<script>
import SuccessModal from "./SuccessModal.vue";
export default {
  components: {
    SuccessModal,
  },
  data() {
    return {
      successMessage: "",
    };
  },
  methods: {
    handleClick() {
      this.successMessage =
        "Спасибо за вашу заявку! Наш менеджер свяжется с вами в ближайшее время.Ожидайте звонка или письма.";
      this.$refs.successmodal.openModal();
    },
  },
};
</script>

<style scoped>
.con {
  background: #777777;
}
.mainText {
  font-family: NotoSerifTamilSlanted;
  font-size: 30px;
  font-style: italic;
  font-weight: 500;
  line-height: 30px;
  color: #03222e;
}

input {
  width: Fixed (551px) px;
  height: Hug (100px) px;
  padding: 15px 25px 15px 25px;
  gap: 10px;
  border-radius: 15px;
  border: 2px;
  font-family: NotoSerifTamilSlanted;
  font-size: 30px;
  font-style: italic;
  font-weight: 500;
  line-height: 30px;
  text-align: left;
  color: #03222eab;
}

.text {
  font-family: NotoSerifTamilSlanted;
  font-size: 20px;
  font-style: italic;
  font-weight: 500;
  line-height: 30px;
  text-align: left;
  color: #03222e7d;
}

.checkbox {
  width: 46px;
  height: 42px;
  gap: 0px;
  border-radius: 5px;
  border: 2px;
}

@media (max-width: 1024px) {
  .nonVis {
    display: none;
  }
}
</style>
