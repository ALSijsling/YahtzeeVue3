<script setup>
  import {ref} from 'vue'
</script>

<template>
  <!-- Top Half Scorecard -->
  <table class="my-10 mx-auto w-1/2">
    <tbody>
        <tr class="bg-sky-300">
          <td class="px-4 py-2 w-3/12 font-bold border border-solid border-black">Part One</td>
          <td class="px-4 py-2 w-2/12 font-bold border border-solid border-black">Score</td>
          <td class="px-4 py-2 w-1/12 font-bold border border-solid border-black">Game 1</td>
          <td class="px-4 py-2 w-1/12 font-bold border border-solid border-black">Game 2</td>
          <td class="px-4 py-2 w-1/12 font-bold border border-solid border-black">Game 3</td>
          <td class="px-4 py-2 w-1/12 font-bold border border-solid border-black">Game 4</td>
          <td class="px-4 py-2 w-1/12 font-bold border border-solid border-black">Game 5</td>
        </tr>
        <tr class="[&>*:nth-child(1)]:bg-sky-100 [&>*:nth-child(2)]:bg-sky-100">
          <td class="px-4 py-2 border border-solid border-black">
            <div class="flex justify-between">
              <p>Aces</p>
              <img src="/Dice1.png" class="h-5" />
            </div>
          </td>
          <td class="px-4 py-2 border border-solid border-black">Total Score of Aces</td>
          <td class="px-4 py-2 border border-solid border-black"></td>
          <td class="px-4 py-2 border border-solid border-black"></td>
          <td class="px-4 py-2 border border-solid border-black"></td>
          <td class="px-4 py-2 border border-solid border-black"></td>
          <td class="px-4 py-2 border border-solid border-black"></td>
        </tr>
        <tr class="[&>*:nth-child(1)]:bg-sky-100 [&>*:nth-child(2)]:bg-sky-100">
          <td class="px-4 py-2 border border-solid border-black">
            <div class="flex justify-between">
              <p>Twos</p>
              <img src="/Dice2.png" class="h-5" />
            </div>
          </td>
          <td class="px-4 py-2 border border-solid border-black">Total Score of Twos</td>
          <td class="px-4 py-2 border border-solid border-black"></td>
          <td class="px-4 py-2 border border-solid border-black"></td>
          <td class="px-4 py-2 border border-solid border-black"></td>
          <td class="px-4 py-2 border border-solid border-black"></td>
          <td class="px-4 py-2 border border-solid border-black"></td>
        </tr>
        <tr class="[&>*:nth-child(1)]:bg-sky-100 [&>*:nth-child(2)]:bg-sky-100">
          <td class="px-4 py-2 border border-solid border-black">
            <div class="flex justify-between">
              <p>Threes</p>
              <img src="/Dice3.png" class="h-5" />
            </div>
          </td>
          <td class="px-4 py-2 border border-solid border-black">Total Score of Threes</td>
          <td class="px-4 py-2 border border-solid border-black"></td>
          <td class="px-4 py-2 border border-solid border-black"></td>
          <td class="px-4 py-2 border border-solid border-black"></td>
          <td class="px-4 py-2 border border-solid border-black"></td>
          <td class="px-4 py-2 border border-solid border-black"></td>
        </tr>
        <tr class="[&>*:nth-child(1)]:bg-sky-100 [&>*:nth-child(2)]:bg-sky-100">
          <td class="px-4 py-2 border border-solid border-black">
            <div class="flex justify-between">
              <p>Fours</p>
              <img src="/Dice4.png" class="h-5" />
            </div>
          </td>
          <td class="px-4 py-2 border border-solid border-black">Total Score of Fours</td>
          <td class="px-4 py-2 border border-solid border-black"></td>
          <td class="px-4 py-2 border border-solid border-black"></td>
          <td class="px-4 py-2 border border-solid border-black"></td>
          <td class="px-4 py-2 border border-solid border-black"></td>
          <td class="px-4 py-2 border border-solid border-black"></td>
        </tr>
        <tr class="[&>*:nth-child(1)]:bg-sky-100 [&>*:nth-child(2)]:bg-sky-100">
          <td class="px-4 py-2 border border-solid border-black">
            <div class="flex justify-between">
              <p>Fives</p>
              <img src="/Dice5.png" class="h-5" />
            </div>
          </td>
          <td class="px-4 py-2 border border-solid border-black">Total Score of Fives</td>
          <td class="px-4 py-2 border border-solid border-black"></td>
          <td class="px-4 py-2 border border-solid border-black"></td>
          <td class="px-4 py-2 border border-solid border-black"></td>
          <td class="px-4 py-2 border border-solid border-black"></td>
          <td class="px-4 py-2 border border-solid border-black"></td>
        </tr>
        <tr class="[&>*:nth-child(1)]:bg-sky-100 [&>*:nth-child(2)]:bg-sky-100">
          <td class="px-4 py-2 border border-solid border-black">
            <div class="flex justify-between">
              <p>Sixes</p>
              <img src="/Dice6.png" class="h-5" />
            </div>
          </td>
          <td class="px-4 py-2 border border-solid border-black">Total Score of Sixes</td>
          <td class="px-4 py-2 border border-solid border-black"></td>
          <td class="px-4 py-2 border border-solid border-black"></td>
          <td class="px-4 py-2 border border-solid border-black"></td>
          <td class="px-4 py-2 border border-solid border-black"></td>
          <td class="px-4 py-2 border border-solid border-black"></td>
        </tr>
        <tr class="[&>*:nth-child(1)]:bg-sky-100">
          <td colspan="2" class="px-4 py-2 border border-solid border-black">
            <div class="flex justify-between">
              <p>Total Points</p>
              <i class='fas fa-arrow-right' style="font-size:24px"></i>
            </div>
          </td>
          <td class="px-4 py-2 border border-solid border-black"></td>
          <td class="px-4 py-2 border border-solid border-black"></td>
          <td class="px-4 py-2 border border-solid border-black"></td>
          <td class="px-4 py-2 border border-solid border-black"></td>
          <td class="px-4 py-2 border border-solid border-black"></td>
        </tr>
        <tr class="[&>*:nth-child(1)]:bg-sky-100 [&>*:nth-child(2)]:bg-sky-100">
          <td class="px-4 py-2 border border-solid border-black">
            <div class="flex justify-between">
              <p>Bonus</p>
              <p class="text-xs text-center">if more than<br> 63 points</p>
            </div>
          </td>
          <td class="px-4 py-2 border border-solid border-black">Total Score of Sixes</td>
          <td class="px-4 py-2 border border-solid border-black"></td>
          <td class="px-4 py-2 border border-solid border-black"></td>
          <td class="px-4 py-2 border border-solid border-black"></td>
          <td class="px-4 py-2 border border-solid border-black"></td>
          <td class="px-4 py-2 border border-solid border-black"></td>
        </tr>
        <tr class="[&>*:nth-child(1)]:bg-sky-100">
          <td colspan="2" class="px-4 py-2 border border-solid border-black">
            <div class="flex justify-between">
              <p>Total Points Of Part One</p>
              <i class='fas fa-arrow-right' style="font-size:24px"></i>
            </div>
          </td>
          <td class="px-4 py-2 border border-solid border-black"></td>
          <td class="px-4 py-2 border border-solid border-black"></td>
          <td class="px-4 py-2 border border-solid border-black"></td>
          <td class="px-4 py-2 border border-solid border-black"></td>
          <td class="px-4 py-2 border border-solid border-black"></td>
        </tr>
    </tbody>
  </table>

  <!-- Bottom Half Scorecard -->
  <table class="my-5 mx-auto w-1/2">
    <tbody>
      <tr class="bg-sky-300">
        <td colspan="7" class="px-4 py-2 font-bold border border-solid border-black">Part Two</td>
      </tr>
      <tr class="[&>*:nth-child(1)]:bg-sky-100 [&>*:nth-child(2)]:bg-sky-100">
          <td class="px-4 py-2 w-3/12 border border-solid border-black">Three of a Kind</td>
          <td class="px-4 py-2 w-2/12 border border-solid border-black">Total of Dice</td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
        </tr>
        <tr class="[&>*:nth-child(1)]:bg-sky-100 [&>*:nth-child(2)]:bg-sky-100">
          <td class="px-4 py-2 w-3/12 border border-solid border-black">Four of a Kind</td>
          <td class="px-4 py-2 w-2/12 border border-solid border-black">Total of Dice</td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
        </tr>
        <tr class="[&>*:nth-child(1)]:bg-sky-100 [&>*:nth-child(2)]:bg-sky-100">
          <td class="px-4 py-2 w-3/12 border border-solid border-black">Full House</td>
          <td class="px-4 py-2 w-2/12 border border-solid border-black">25 Points</td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
        </tr>
        <tr class="[&>*:nth-child(1)]:bg-sky-100 [&>*:nth-child(2)]:bg-sky-100">
          <td class="px-4 py-2 w-3/12 border border-solid border-black">
            <div class="flex justify-between">
              <p>Small Straight</p>
              <p class="text-xs text-center">Sequence<br>of 4 dice</p>
            </div>
          </td>
          <td class="px-4 py-2 w-2/12 border border-solid border-black">30 Points</td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
        </tr>
        <tr class="[&>*:nth-child(1)]:bg-sky-100 [&>*:nth-child(2)]:bg-sky-100">
          <td class="px-4 py-2 w-3/12 border border-solid border-black">
            <div class="flex justify-between">
              <p>Large Straight</p>
              <p class="text-xs text-center">Sequence<br>of 5 dice</p>
            </div>
          </td>
          <td class="px-4 py-2 w-2/12 border border-solid border-black">40 Points</td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
        </tr>
        <tr class="[&>*:nth-child(1)]:bg-sky-100 [&>*:nth-child(2)]:bg-sky-100">
          <td class="px-4 py-2 w-3/12 border border-solid border-black">
            <div class="flex justify-between">
              <p>Yahtzee</p>
              <p class="text-xs text-center">5 of a<br>kind</p>
            </div>
          </td>
          <td class="px-4 py-2 w-2/12 border border-solid border-black">50 Points</td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
        </tr>
        <tr class="[&>*:nth-child(1)]:bg-sky-100 [&>*:nth-child(2)]:bg-sky-100">
          <td class="px-4 py-2 w-3/12 border border-solid border-black">Chance</td>
          <td class="px-4 py-2 w-2/12 border border-solid border-black">Total of Dice</td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
        </tr>
        <tr class="[&>*:nth-child(1)]:bg-sky-100">
          <td colspan="2" class="px-4 py-2 w-3/12 border border-solid border-black">
            <div class="flex justify-between">
              <p>Total Points of Part Two</p>
              <i class='fas fa-arrow-right' style="font-size:24px"></i>
            </div>
          </td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
        </tr>
        <tr class="[&>*:nth-child(1)]:bg-sky-100">
          <td colspan="2" class="px-4 py-2 w-2/12 border border-solid border-black">
            <div class="flex justify-between">
              <p>Total Points of Part One</p>
              <i class='fas fa-arrow-right' style="font-size:24px"></i>
            </div>
          </td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
        </tr>
        <tr class="[&>*:nth-child(1)]:bg-sky-100">
          <td colspan="2" class="px-4 py-2 w-3/12 border border-solid border-black">
            <div class="flex justify-between">
              <p class="font-bold">Total Score</p>
              <i class='fas fa-arrow-right' style="font-size:24px"></i>
            </div>
          </td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
          <td class="px-4 py-2 w-1/12 border border-solid border-black"></td>
        </tr>
    </tbody>
  </table>
</template>
