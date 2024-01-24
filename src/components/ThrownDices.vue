<script setup>
  import {ref} from 'vue'
</script>

<template>
  <table class="flex justify-center my-10">
    <tr>
        <td><img src="/Dice0.png" class="h-20"></td>
        <td><img src="/Dice0.png" class="h-20"></td>
        <td><img src="/Dice0.png" class="h-20"></td>
        <td><img src="/Dice0.png" class="h-20"></td>
        <td><img src="/Dice0.png" class="h-20"></td>
    </tr>
  </table>

  <div class="flex justify-center">
    <button
        class="px-6 py-2 text-xl bg-lime-600 rounded-xl border-2 border-solid border-lime-800"
        @click=""
        >
        Roll Dice
    </button>
  </div>
</template>
