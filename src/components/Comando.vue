<template>
  <div class="comand-group">
    <div class="comand">
      <span>-1⚡</span>
      <div class="iconUp">
        <h4><i class="fas up fa-arrow-left"></i></h4>
      </div>
      <span>Em frente</span>
    </div>
    <div class="comand">
      <span>-1⚡</span>
      <div class="iconleft">
        <h4><i class="fas fa-arrow-left"></i></h4>
      </div>
      <span>Vire</span>
    </div>
    <div class="comand">
      <span>-1⚡</span>
      <div class="repeat">
        <h4><i class="fas fa-redo"></i></h4>
      </div>
      <span>Repete</span>
    </div>
  </div>
</template>

<script>
import seta from "../assets/seta.png";
import energia from "../assets/energia.jpg";
import vire from "../assets/vire.png";

export default {
  data() {
    return {
      seta,
      energia,
      vire,
    };
  },
};
</script>

<style scoped>
.comand-group {
  display: flex;
  gap: 1rem;
  color: black;
}
.up {
  transform: rotateZ(90deg);
}
.iconUp {
  animation: animUp 0.5s infinite linear alternate;
  transform-origin: center;
  transform-box: fill-box;
}
@keyframes animUp {
  from {
    transform: translateY(0px);
    color: blue;
  }
  to {
    transform: translateY(10px);
    color: black;
  }
}

.iconleft {
  animation: animLeft 0.5s infinite linear alternate;
  transform-origin: center;
  transform-box: fill-box;
}
@keyframes animLeft {
  from {
    transform: translateX(0px);
    color: blue;
  }
  to {
    transform: translateX(-10px);
    color: black;
  }
}

.repeat{
 
    animation: girando 1.5s infinite linear;
    transform-origin: center;
    transform-box: fill-box;

}

@keyframes girando{
    from{
        transform: rotateZ(0deg);
        color: blue;
    }
    to{
        transform: rotateZ(360deg);
    }

    to{

    }
    
}

.comand {
  width: 12rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  font-size: 2rem;
  gap: 0.6rem;
  background: rgb(255, 255, 255);
  border-radius: 0.8rem;
  box-shadow: 1px 1px 16px rgba(0, 0, 0, 0.815);
  padding: 0.7rem;
}

.icone {
  width: 1rem;
  height: 1rem;
}

.comand img {
  width: 4rem;
  height: 2rem;
}
</style>