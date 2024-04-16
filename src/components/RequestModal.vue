<template>
  <div v-if="showModal" class="modal-overlay">
    <div class="modal flex flex-col items-center space-y-4">
      <span class="close" @click="closeModal">&times;</span>
      <div class="modal-header">
        <slot name="header" class="header">Default Header</slot>
      </div>
      <div class="modal-body flex flex-col items-center space-y-12">
        <slot name="body">Default Body</slot>
      </div>
      <div class="modal-footer">
        <slot name="footer">
          <div
            class="flex flex-col items-center max-w-sm w-2/3 mx-auto text-center space-y-4"
          >
            <button @click="handleClick">Перезвонить</button>
            <span>
              Нажимая кнопку “Перезвонить”, вы соглашаетесь с обработкой
              персональных данных
            </span>
          </div>
        </slot>
      </div>
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
  data() {
    return {
      showModal: false,
      successMessage: "",
    };
  },
  components: {
    SuccessModal,
  },
  methods: {
    handleClick() {
      this.successMessage =
        "Спасибо за вашу заявку! Наш менеджер свяжется с вами в ближайшее время.Ожидайте звонка или письма.";
      this.$refs.successmodal.openModal();
      this.closeModal();
    },
    openModal() {
      this.showModal = true;
    },
    closeModal() {
      this.showModal = false;
    },
  },
};
</script>

<style scoped>
.modal-overlay {
  position: fixed;
  top: -1rem;
  left: 0;
  width: 100%;
  height: 110vh;
  background-color: rgba(0, 0, 0, 0.5);
  display: flex;
  justify-content: center;
  align-items: center;
}

.modal {
  border-top: 15px solid #e3b253;
  background-color: white;
  padding: 40px 20px;
  border-radius: 8px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
  max-width: 500px;
}

.close {
  position: absolute;
  top: 10px;
  right: 10px;
  cursor: pointer;
}

.modal-header,
.modal-body,
.modal-footer {
  margin-bottom: 10px;
}

.modal-header {
  font-family: NotoSerifTamilSlanted;
  font-size: 30px;
  font-style: italic;
  font-weight: 500;
  line-height: 40px;
  text-align: left;
}

.modal-body {
  font-family: Inter;
  font-size: 20px;
  font-weight: 500;
  line-height: 24.2px;
  text-align: left;
  color: #00000057;
}

.modal-footer button {
  background: #e3b253;
  width: Fixed (45px) px;
  height: Hug (39px) px;
  padding: 1rem;
  gap: 10px;
  border-radius: 5px;
  color: #fff;
  cursor: pointer;
}

.header {
  font-family: Inter;
  font-size: 35px;
  font-weight: 500;
  line-height: 42.36px;
  text-align: center;
  color: #1e2151;
}
</style>
