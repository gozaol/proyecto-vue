<template>
    <h1>Mierda Vue</h1>
    <p><img src="/src/components/imagenes/Screenshot_1.jpg" alt="" >Cesta <span >{{ contador }}</span> Productos</p>
  
    <button @click="incrementar">Incrementar</button>
    <button @click="decrementar">Decrementar</button>
</template>
  
  <script  setup>
  import {ref} from 'vue';
  const contador = ref(0);
  
  const incrementar = ()=>{
    contador.value++;
  }
  
  const decrementar = ()=>{
    if (contador.value > 0)
    contador.value--;
    else
      contador.value=0;
    
  }
  
  </script>
  <style scoped>
  img{
    width: 50px;
  }
  p{
    font-family: Verdana, Geneva, Tahoma, sans-serif;
  }
  span{
    color:red;
    font-weight: bold;
  }
  </style>