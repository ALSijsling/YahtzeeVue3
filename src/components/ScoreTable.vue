<script setup>
  import {ref} from 'vue'
  import TableData from './TableData.vue'
  import TableHead from './TableHead.vue'
  import TableRow from './TableRow.vue'
  import TableRowSpan from './TableRowSpan.vue'
</script>

<template>
  <!-- Top Half Scorecard -->
  <table class="my-10 mx-auto w-1/2">
    <tbody>
      <TableHead>
        <TableData class="w-3/12">Part One</TableData>
        <TableData class="w-2/12">Score</TableData>
        <TableData class="w-1/12">Game 1</TableData>
        <TableData class="w-1/12">Game 2</TableData>
        <TableData class="w-1/12">Game 3</TableData>
        <TableData class="w-1/12">Game 4</TableData>
        <TableData class="w-1/12">Game 5</TableData>
      </TableHead>
      <TableRow>
        <TableData>
          <div class="flex justify-between">
            <p>Aces</p>
            <img src="/Dice1.png" class="h-5" />
          </div>
        </TableData>
        <TableData>Total Score of Aces</TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
      </TableRow>
      <TableRow>
        <TableData>
          <div class="flex justify-between">
            <p>Twos</p>
            <img src="/Dice2.png" class="h-5" />
          </div>
        </TableData>
        <TableData>Total Score of Twos</TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
      </TableRow>
      <TableRow>
        <TableData>
          <div class="flex justify-between">
            <p>Threes</p>
            <img src="/Dice3.png" class="h-5" />
          </div>
        </TableData>
        <TableData>Total Score of Threes</TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
      </TableRow>
      <TableRow>
        <TableData>
          <div class="flex justify-between">
            <p>Fours</p>
            <img src="/Dice4.png" class="h-5" />
          </div>
        </TableData>
        <TableData>Total Score of Fours</TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
      </TableRow>
      <TableRow>
        <TableData>
          <div class="flex justify-between">
            <p>Fives</p>
            <img src="/Dice5.png" class="h-5" />
          </div>
        </TableData>
        <TableData>Total Score of Fives</TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
      </TableRow>
      <TableRow>
        <TableData>
          <div class="flex justify-between">
            <p>Sixes</p>
            <img src="/Dice6.png" class="h-5" />
          </div>
        </TableData>
        <TableData>Total Score of Sixes</TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
      </TableRow>
      <TableRowSpan>
        <TableData colspan="2">
          <div class="flex justify-between">
            <p>Total Points</p>
            <i class='fas fa-arrow-right' style="font-size:24px"></i>
          </div>
        </TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
      </TableRowSpan>
      <TableRow>
        <TableData>
          <div class="flex justify-between">
            <p>Bonus</p>
            <p class="text-xs text-center">if more than<br> 63 points</p>
          </div>
        </TableData>
        <TableData>Total Score of Sixes</TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
      </TableRow>
      <TableRowSpan>
        <TableData colspan="2">
          <div class="flex justify-between">
            <p>Total Points Of Part One</p>
            <i class='fas fa-arrow-right' style="font-size:24px"></i>
          </div>
        </TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
      </TableRowSpan>
    </tbody>
  </table>

  <!-- Bottom Half Scorecard -->
  <table class="my-5 mx-auto w-1/2">
    <tbody>
      <TableHead>
        <TableData colspan="7">Part Two</TableData>
      </TableHead>
      <TableRow>
        <TableData class="w-3/12">Three of a Kind</TableData>
        <TableData class="w-2/12">Total of Dice</TableData>
        <TableData class="w-1/12"></TableData>
        <TableData class="w-1/12"></TableData>
        <TableData class="w-1/12"></TableData>
        <TableData class="w-1/12"></TableData>
        <TableData class="w-1/12"></TableData>
      </TableRow>
      <TableRow>
        <TableData>Four of a Kind</TableData>
        <TableData>Total of Dice</TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
      </TableRow>
      <TableRow>
        <TableData>Full House</TableData>
        <TableData>25 Points</TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
      </TableRow>
      <TableRow>
        <TableData>
          <div class="flex justify-between">
            <p>Small Straight</p>
            <p class="text-xs text-center">Sequence<br>of 4 dice</p>
          </div>
        </TableData>
        <TableData>30 Points</TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
      </TableRow>
      <TableRow>
        <TableData>
          <div class="flex justify-between">
            <p>Large Straight</p>
            <p class="text-xs text-center">Sequence<br>of 5 dice</p>
          </div>
        </TableData>
        <TableData>40 Points</TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
      </TableRow>
      <TableRow>
        <TableData>
          <div class="flex justify-between">
            <p>Yahtzee</p>
            <p class="text-xs text-center">5 of a<br>kind</p>
          </div>
        </TableData>
        <TableData>50 Points</TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
      </TableRow>
      <TableRow>
        <TableData>Chance</TableData>
        <TableData>Total of Dice</TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
      </TableRow>
      <TableRowSpan>
        <TableData colspan="2">
          <div class="flex justify-between">
            <p>Total Points of Part Two</p>
            <i class='fas fa-arrow-right' style="font-size:24px"></i>
          </div>
        </TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
      </TableRowSpan>
      <TableRowSpan>
        <TableData colspan="2">
          <div class="flex justify-between">
            <p>Total Points of Part One</p>
            <i class='fas fa-arrow-right' style="font-size:24px"></i>
          </div>
        </TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
      </TableRowSpan>
      <TableRowSpan>
        <TableData colspan="2">
          <div class="flex justify-between">
            <p class="font-bold">Total Score</p>
            <i class='fas fa-arrow-right' style="font-size:24px"></i>
          </div>
        </TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
      </TableRowSpan>
    </tbody>
  </table>
</template>
