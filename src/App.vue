<template>
  <v-app>
    <div>
      <img class="background-pic" :src="require('./assets/logo.svg')">
      <div class="content-block">
        <img class="content-block__logo" :src="require('./assets/logo-name.svg')">
        <div>Совсем скоро тут появится информация о нашем новом продукте</div>
        <div class="content-block__scnd-line">Вы можете перейти на <a href="https://st-inv.ru/" style="color: #557745">главную страницу</a>, чтобы ознакомиться с остальными продуктами</div>
        <v-btn @click="formOpening('true')" color="#A5CD39" class="button">Демо</v-btn>
      </div>
    </div>

    <div>
      <v-overlay
        v-if="overlay === 'true'"
      >
        <div class="card">
          <div class="card__title d-flex justify-space-between mb-10">
            <h1>Заказать демо</h1>
            <v-icon @click="formOpening('false')" color="#FF2400" class="pointer">mdi-close</v-icon>
          </div>
          <div class="card__content">
              <div class="d-flex align-center mb-3">Компания</div>
              <input class="mb-3 mr-1" style="padding: 10px 5px 10px 5px;" type="text" id="value" placeholder="Укажите название компании, номер ИНН или ОГРН">
              
              <div class="d-flex align-center mb-3">ФИО</div>
              <input class="mb-3 mr-1" style="padding: 10px 5px 10px 5px;" type="text" id="value" placeholder="Укажите Фамилию Имя Отчество">
              
              <div class="d-flex align-center mb-3">Email</div>
              <input class="mb-3 mr-1" style="padding: 10px 5px 10px 5px;" type="text" id="value" placeholder="Укажите Email">
            
              <div class="d-flex align-center mb-3">Телефон</div>
              <input class="mb-3 mr-1" style="padding: 10px 5px 10px 5px;" type="text" id="value" placeholder="Укажите Ваш номер телефона">
              
              <div class="d-flex align-center mb-3">Количество свиноматок</div>
              <input class="mb-3 mr-1" style="padding: 10px 5px 10px 5px;" type="text" id="value" placeholder="Укажите количество свиноматок">
          </div>
          <div class="d-flex align-center mb-5">
            <input type="checkbox" class="checkbox mr-3"> 
            <div>Я согласен с <a href="https://drive.google.com/file/d/1Mt36_m0zbEqANmhw4xNKrtNFMX9mK8k0/view">условиями обработки</a> персональных данных</div>
          </div>
          <v-btn color="#A5CD39">Заказать</v-btn>
        </div>
      </v-overlay>
    </div>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  components: {
    
  },

  data: () => ({
    overlay: 'false',
    pdfIsOpen: 'false'
  }),
  methods: {
    formOpening(value) {
      this.overlay = value
    },
    openPDF(value) {
      this.pdfIsOpen = value
    }
  },
  props: [
    
  ],
  mounted() {
    
  }
};
</script>

<style scoped>
a {
  text-decoration: none;
  color: green;
}
.background-pic {
  position: fixed;
  z-index: 1;
  left: 46vw;
  height: 100vh;
  bottom: 0vh;
}
.content-block {
  padding: 15vw 60vw 0vw 13vw;
  font-family: "Arial";
  font-weight: 700;
  font-size: 3vh;
  color: #404040;
  display: flex;
  flex-direction: column;
  row-gap: 2vh;
  line-height: 43.2px;
}
.content-block__logo {
  margin-bottom: 30px;
}
.content-block__scnd-line {
  font-size: 2vh;
}
.content-block__clickable {
  color: #557745;
}
.button {
  background-color: #A5CD39;
  border-radius: 22px;
  width: 30%;
  text-align: center;
  color: #FFFFFF;
  font-size: 20px;
  border: 1px #404040 solid
}
.card {
  box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.25);
  border-radius: 10px;
  background-color: #fff;
  color: #000;
  padding: 50px;
}
.card__content {
  display: grid;
  grid-template-columns: 1fr 2.25fr;
  column-gap: 25px;
}
.pdf {
  position: absolute !important;
  z-index: 2;
}
</style>