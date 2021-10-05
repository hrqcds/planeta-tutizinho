<template>
  <div class="car-group">
    <img class="car" :src="this.$props.imagem" />
    <div class="car-progress-group">
      <button type="button" :class="nameButton" @click="diminuir">-</button>
      <div :class="cores"></div>
      <button type="button" :class="nameButton" @click="adicionar">+</button>
    </div>
    <button @click="reset">Reset</button>
  </div>
</template>

<script>
export default {
  props: ["imagem", "cor"],
  computed: {
    cores() {
      return `progress-bar_${this.$props.cor}`;
    },
    nameButton() {
      return `button_${this.$props.cor}`;
    },
  },
  data() {
    return {
      progresso: 100,
    };
  },
  methods: {
    adicionar: function () {
      const progress = document.querySelector(
        `.progress-bar_${this.$props.cor}`
      );

      if (this.progresso === 100) {
        this.progresso = 100;
        return;
      }

      this.progresso += 5;
      progress.style.setProperty("--progress", this.progresso);
    },

    diminuir: function () {
      const progress = document.querySelector(
        `.progress-bar_${this.$props.cor}`
      );

      if (this.progresso === 0) {
        this.progresso = 0;
        return;
      }

      this.progresso -= 5;
      progress.style.setProperty("--progress", this.progresso);
    },
    reset: function () {
      const progress = document.querySelector(
        `.progress-bar_${this.$props.cor}`
      );
      this.progresso = 100
      progress.style.setProperty("--progress", this.progresso);
    },
  },
};
</script>

<style scoped>
.car {
  width: 6rem;
  height: 3rem;
}

.car-progress-group {
  display: flex;
  justify-content: center;
  align-items: center;
  color: black;
}

.car-progress-group button {
  margin: 0 5px;
  width: 2rem;
  height: 2rem;
  background: white;
  font-size: 2rem;
  border: none;
  box-shadow: 1px 1px 3px black;
  border-radius: 50%;
  transition: filter 0.5s;
  display: flex;
  align-items: center;
  justify-content: center;
}

.car-progress-group button:hover {
  filter: brightness(0.8);
  cursor: pointer;
}

.progress-bar_green {
  --progress: 100;
  height: 50px;
  padding: 5px;
  width: 40rem;
  border: 1px solid black;
  box-shadow: 1px 1px 8px black;
  background-color: #ccc;
  display: flex;
}

.progress-bar_green::before {
  content: "ENGENHARIA";
  width: calc(var(--progress) * 1%);
  display: grid;
  align-items: center;
  background: #34a853;
}

.progress-bar_blue {
  --progress: 100;
  height: 50px;
  padding: 5px;
  width: 40rem;
  border: 1px solid black;
  box-shadow: 1px 1px 8px black;
  background-color: #ccc;
  display: flex;
}

.progress-bar_blue::before {
  content: "TUTILABS";
  width: calc(var(--progress) * 1%);
  display: grid;
  align-items: center;
  background: #4285f4;
}

.progress-bar_yellow {
  --progress: 100;
  height: 50px;
  padding: 5px;
  width: 40rem;
  border: 1px solid black;
  box-shadow: 1px 1px 8px black;
  background-color: #ccc;
  display: flex;
}

.progress-bar_yellow::before {
  content: "RH";
  width: calc(var(--progress) * 1%);
  display: grid;
  align-items: center;
  background: #fbbc05;
}

.progress-bar_lilac {
  --progress: 100;
  height: 50px;
  padding: 5px;
  width: 40rem;
  border: 1px solid black;
  box-shadow: 1px 1px 8px black;
  background-color: #ccc;
  display: flex;
}

.progress-bar_lilac::before {
  content: "SGQ";
  display: grid;
  align-items: center;
  width: calc(var(--progress) * 1%);
  background: #bb44f2;
}

.progress-bar_red {
  --progress: 100;
  height: 50px;
  padding: 5px;
  width: 40rem;
  border: 1px solid black;
  box-shadow: 1px 1px 8px black;
  background-color: #ccc;
  display: flex;
}

.progress-bar_red::before {
  content: "MANUTENÇÃO";
  display: grid;
  align-items: center;
  width: calc(var(--progress) * 1%);
  background: #ea4335;
}
</style>