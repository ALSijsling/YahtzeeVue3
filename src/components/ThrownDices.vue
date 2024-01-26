<script setup>
  import {ref} from 'vue'
  const emit = defineEmits(['thrown-dices'])

  const dices = ref()
  const diceImg = [
    '/Dice1.png',
    '/Dice2.png',
    '/Dice3.png',
    '/Dice4.png',
    '/Dice5.png',
    '/Dice6.png'
  ]

  const throwDice = ()=>{
    dices.value = []
    for (let d=0; d<5; d++){
      let die = Math.floor(Math.random() * 6) + 1
      dices.value.push(die)
    }
    emit('thrown-dices', dices.value)
  }
</script>

<template>
  <table class="flex justify-center my-10">
    <tr v-if="dices" v-for="dice in dices">
      <td><img :src="diceImg[dice-1]" class="h-20"></td>
    </tr>
    <tr v-else>
      <td><img src="/Dice0.png" class="h-20"></td>
      <td><img src="/Dice0.png" class="h-20"></td>
      <td><img src="/Dice0.png" class="h-20"></td>
      <td><img src="/Dice0.png" class="h-20"></td>
      <td><img src="/Dice0.png" class="h-20"></td>
    </tr>
  </table>

  <div class="flex justify-center">
    <button
      @click="throwDice"
      class="px-6 py-2 text-xl bg-lime-600 rounded-xl border-2 border-solid border-lime-800"
      >
      Roll Dice
    </button>
  </div>
</template>
