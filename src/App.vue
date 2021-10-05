<template>
  <div>
    <div class="navbar">
      <div>
        <img class="logo" :src="logoTuti" alt="logo tutiplast" />
      </div>
      <h1>Planeta Tutizinho</h1>
      <div>
        <img class="logo" :src="logo" alt="logo tutilabs" />
      </div>
    </div>

    <section class="tutizinho">
      <div class="car-group_principal">
        <Car :imagem="amarelo" cor="yellow" />
        <Car :imagem="azul" cor="blue" />
        <Car :imagem="vermelho" cor="red" />
        <Car :imagem="lilas" cor="lilac" />
        <Car :imagem="verde" cor="green" />
      </div>
      <div class="instrucoes">
        <Regras />
        <Comando />
      </div>
    </section>
  </div>
</template>

<script>
//Import de components
import Car from "./components/Car.vue";
import Comando from "./components/Comando.vue";
import Regras from "./components/Regras.vue";

//Import de imagens
import amarelo from "./assets/carAmarelo.svg";
import azul from "./assets/carAzul.svg";
import vermelho from "./assets/carVermelho.svg";
import lilas from "./assets/carLilas.svg";
import verde from "./assets/carVerde.svg";
import logo from "./assets/Tutilabs-logo.png";
import logoTuti from "./assets/logo-tuti.png";

export default {
  name: "App",
  components: {
    Car,
    Comando,
    Regras,
  },
  data() {
    return {
      amarelo,
      azul,
      vermelho,
      lilas,
      verde,
      logo,
      logoTuti,
    };
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Hachi+Maru+Pop&display=swap");

#app {
  font-family: sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}

* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

body {
  background-image: url("./assets/bg.jpg");
  background-size: cover;
  color: white;
}

.navbar {
  height: 10vh;
  display: flex;
  align-items: center;
  justify-content: space-evenly;
  font-family: "Hachi Maru Pop", cursive;
}

.tutizinho {
  display: flex;
  align-items: center;
  justify-content: space-around;
  width: 100vw;
  height: 90vh;
}

.instrucoes {
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: center;
  width: 100%;
  height: 100%;
}

.car-group_principal {
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100%;
  border-radius: 0 2rem 2rem 0;
  background: rgba(255, 255, 255, 0.158);
  box-shadow: 3px 0 8px rgba(0, 0, 0, 0.418);
}

.logo {
  padding: 1rem;
  width: 10rem;
}
</style>
