<template>
         <ul>
              <li>
                   
                        <button type="button" @click="()=>{placar--}">-</button> 
                           <p> {{this.$props.titulo}}: {{placar}} </p>
                        <button @click="()=>{placar++}">+</button> 
              </li>
          </ul>
</template>

<script>
export default {

    props: ["titulo"],
    data(){
        return {
            placar: 0
        }
    }

}
</script>

<style scoped>

button{
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

 button:hover{
    filter: brightness(0.8);
    cursor: pointer;
}

ul{
    list-style: none;
}

li{
    display: flex;
    width: 15rem;
    justify-content: space-between;
    align-items: center;
}



</style>