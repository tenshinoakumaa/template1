<template>
  <div class="con flex flex-col items-center py-28 space-y-14">
    <div class="flex flex-row items-end max-w-md lg:max-w-6xl">
      <div
        class="miniDiv flex flex-col items-center justify-center p-4 space-y-2"
      >
        <span class="miniDivMainText">ЦЕНА</span>
        <span class="miniDivSecondText">текст текст</span>
      </div>
      <div
        class="bigDiv p-4 flex flex-col justify-center items-center p-4 space-y-2"
      >
        <span class="bigDivMainText">ЦЕНА</span>
        <span class="bigDivSecondText">текст текст</span>
      </div>
      <div
        class="miniDiv2 flex flex-col justify-center items-center p-4 space-y-2"
      >
        <span class="miniDivMainText">ЦЕНА</span>
        <span class="miniDivSecondText">текст текст</span>
      </div>
    </div>
    <button class="greenButton">ЗАКАЗАТЬ</button>
  </div>
</template>

<style scoped>
.con {
  background: #656565e0;
}
.miniDiv {
  background: #d9d9d9;
  height: 128px;
  border-radius: 15px 0px 0px 15px;
}
.miniDiv2 {
  background: #d9d9d9;
  height: 128px;
  border-radius: 0px 15px 15px 0px;
}
.bigDiv {
  background: #edecec;
  width: 397px;
  height: 196px;
  gap: 0px;
  border-radius: 15px 15px 0px 0px;
}

.bigDivMainText {
  font-family: Inter;
  font-size: 45px;
  font-style: italic;
  font-weight: 400;
  line-height: 54.46px;
  text-align: center;
}

.bigDivSecondText {
  font-family: Inter;
  font-size: 24px;
  font-style: italic;
  font-weight: 400;
  line-height: 29.05px;
  text-align: center;
}

.miniDivMainText {
  font-family: Inter;
  font-size: 35px;
  font-style: italic;
  font-weight: 400;
  line-height: 42.36px;
  text-align: center;
}
.miniDivSecondText {
  font-family: Inter;
  font-size: 24px;
  font-style: italic;
  font-weight: 400;
  line-height: 29.05px;
  text-align: center;
}
</style>
