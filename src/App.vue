<script setup>
import { ref } from "vue";
import ThrownDices from "./components/ThrownDices.vue";
import ScoreTable from "./components/ScoreTable.vue";

const header = ref("Yahtzee");
const thrownDices = ref([]);

const dices = (die) => {
  thrownDices.value = die;
};
</script>

<template>
  <div class="flex justify-center">
    <img src="./assets/logo.png" class="h-16" alt="Yahtzee Logo" />
    <h1 class="text-5xl font-bold text-center text-sky-800">{{ header }}</h1>
  </div>

  <!-- TODO: uitzoeken hoe je dit met een v-model kunt oplossen (het doorgeven van dices),
  zodat je zonder de dices functie toe kunt -->
  <ThrownDices @thrown-dices="dices" />

  <ScoreTable :thrown-dices="thrownDices" />
</template>
