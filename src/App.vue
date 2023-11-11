<script setup>
import {ref } from 'vue'
let name= ref('Уважаемые Александр и Кристина')
let table = ref('1')
</script>

<template>
  <div class="wrapper_h_B">
    <div class="walpers_block">
      <div class="name">{{name}}</div>
      <div class="text">
        Приглашаем Вас <span>18 ноября</span> к <span>16:00</span> в ресторан
        <span>«Онегин»</span> по адресу: г. Ставрополь, Михайловское шоссе 28а.
        Вас ждет веселый праздник в кругу друзей. В программе зажигательная
        ведущая, сюрпризы, подарки, танцы, ну и, конечно, непредсказуемая
        реакция именинника на происходящее. Не задерживайтесь, на входе вас
        встретят удивительные персонажи и угостят игристым. Прихватите с собой
        хорошее настроение, это поможет фотографу и видеографу запечатлеть
        лучшие моменты вечера.

        <p class="table">P.s. Ваш столик №<span>{{ table }}</span></p>
      </div>
      <!-- <div class="block data">18/11/2023</div> -->
    </div>
  </div>

  <div>
    <label for="name">Кому:</label><br>
    <input type="text" id="name" v-model="name" />
  </div>

  <div>
    <label for="table">Номер столика:</label> <br>
    <input type="text" id="table" v-model="table" />
  </div>
</template>

<style scoped>
.wrapper_h_B {
  width: 500px;
  height: 90vh;
  background-image: url("./assets/img/HB1.jpg");
  background-size: cover;
  color: white;
  font-family: "Pattaya", sans-serif;
}
.walpers_block {
  display: flex;
  flex-direction: column;
  justify-content: center;
  height: 100%;
  align-items: center;
  background-image: linear-gradient(
    to right,
    #462523 0,
    #cb9b51 22%,
    #f6e27a 45%,
    #f6f2c0 50%,
    #f6e27a 55%,
    #cb9b51 78%,
    #462523 100%
  );
  color: transparent;
  -webkit-background-clip: text;
  padding-top: 145px;
}
.name {
  font-size: 23px;
  font-weight: bold;
  border-bottom: 2px solid goldenrod;
  margin-bottom: 5px;
}
.text {
  width: 368px;
  text-align: center;
  font-size: 15px;
  line-height: 24px;
}

span {
  font-weight: 600;
  font-size: 18px;
}

.table {
  margin-top: 10px;
  font-size: 19px;
  font-weight: 600;
}

input {
  width: 300px;
}
</style>
