<template>
  <v-app>
    <div>
      <img class="background-pic" :src="require('./assets/logo.svg')">
      <div class="content-block">
        <img class="content-block__logo" :src="require('./assets/logo-name.svg')">
        <div>Совсем скоро тут появится информация о нашем новом продукте</div>
        <div class="content-block__scnd-line">Вы можете перейти на <a href="https://st-inv.ru/" style="color: #557745">главную страницу</a>, чтобы ознакомиться с остальными продуктами</div>
        <v-btn color="#A5CD39" class="button">Демо</v-btn>
      </div>
    </div>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  components: {
    
  },

  data: () => ({
    
  }),
  methods: {
    
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
</style>