<script setup>
import { ref } from 'vue';
const contador = ref(10)
const contador2 = ref(10)
</script>

<template>
  <div class="info">
    <hr />
    Contador: {{ contador }}
    <button @click="contador++">+</button>
    <button @click="contador--">-</button>   
    <hr />
  </div>
  <div class="info2">
    <hr />
    Contador2: {{ contador2 }}
    <button @click="contador2++">+</button>
    <button @click="contador2--">-</button>   
    <hr />
  </div>
  <div class="conta">
    <div v-if="contador + contador2 > 10" class="maior">a soma do contador é maior que 10</div>
    <div v-else-if="contador + contador2 < 10" class="menor">a soma do contador é menor que 10</div>
    <div v-else class="igual">a soma do contador é igaul a 10</div>
    </div>

</template>
<style scoped>
.info {
  background-color: rgba(35,12,22,1);
  padding: 20px 30px;
  color: rgb(183, 210, 219);
  border-radius: 10px;
}
.conta {
  background-color: rgba(35,12,22,1);
  padding: 20px 30px;
  color: rgb(183, 210, 219);
  border-radius: 10px;
}
.info2 {
  background-color: rgba(35,12,22,1);
  padding: 20px 30px;
  color: rgb(183, 210, 219);
  border-radius: 10px;
}
</style>