<template>
  <div class="rules-group">
        <div class="rules">
            <h1>Regras</h1>
            <h2>
                As peças movem os carros,
                
                carro anda apenas em uma direção,
                
                cada peça tem um custo de energia pro carro
            </h2>
        </div>
        <div class="luanObrabo">
            <h1>Placar</h1>
            <Placar titulo="Amarelo"/>
            <Placar titulo="Azul"/>
            <Placar titulo="Vermelho"/>
            <Placar titulo="Lilas"/>
            <Placar titulo="Verde"/>
        </div>
  </div>
</template>

<script>
import Placar from "./Placar.vue"

export default {
    components: {Placar}


}
</script>

<style>

ul{
    list-style: none;
}
.luanObrabo{
    display: grid;
    justify-content: center;
    grid-gap: 1rem;

    margin-top: .7rem;
    border: 2px solid white;
    padding: 1rem;
    border-radius: .8rem;
    background: rgba(255, 255, 255, 0.158);
}
.rules-group{
    padding: 0 2rem;
}

.rules{
    font-size: 16px;
    color: white;
    text-align: left;
}
h2{
    font-weight: 300;
}
</style>