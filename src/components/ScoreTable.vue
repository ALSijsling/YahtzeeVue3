<script setup>
import { computed, ref } from "vue";
import TableData from "./TableData.vue";
import TableHead from "./TableHead.vue";
import TableRow from "./TableRow.vue";
import TableRowSpan from "./TableRowSpan.vue";

const props = defineProps(["thrownDices"]);

const dices = ref(props.thrownDices);

const count = computed(() => {
  let countObj = {
    1: 0,
    2: 0,
    3: 0,
    4: 0,
    5: 0,
    6: 0,
  };

  props.thrownDices.forEach((die) => {
    countObj[die]++;
  });

  return countObj;
});

const countDuplicates = (num) => {
  let dice = Object.values(count.value)
  if(dice.includes(num))
  return true
};

const numScoreTotal = computed(() =>
  props.thrownDices.reduce((acc, item) => (acc = acc + item), 0)
);
const bonusScore = computed(() => (numScoreTotal.value > 63 ? 35 : 0));

const bottomScore = computed(
  () =>
    chance.value +
    threeKind.value +
    fourKind.value +
    yahtzee.value +
    fullHouse.value +
    smallStraight.value +
    largeStraight.value
);

// bottomscores
const chance = computed(() =>
  props.thrownDices.reduce((total, value) => total + value, 0)
);
const threeKind = computed(() =>
  countDuplicates(3) || countDuplicates(4) || countDuplicates(5)
    ? chance.value
    : 0
);
const fourKind = computed(() =>
  countDuplicates(4) || countDuplicates(5) ? chance.value : 0
);
const yahtzee = computed(() => (countDuplicates(5) ? chance.value : 0));
const fullHouse = computed(() =>
  countDuplicates(2) && countDuplicates(3) ? 25 : 0
);

const smallStraight = computed(() => {
  dices.value.sort();
  if (/1234|2345|3456/.test(dices.value.join("").replace(/(.)\1/, "$1")))
    return 30;
  else return 0;
});

const largeStraight = computed(() => {
  dices.value.sort();
  if (/12345|23456/.test(dices.value.join(""))) return 40;
  else return 0;
});
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
        <TableData>{{ count[1] }}</TableData>
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
        <TableData>{{ count[2] * 2 }}</TableData>
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
        <TableData>{{ count[3] * 3 }}</TableData>
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
        <TableData>{{ count[4] * 4 }}</TableData>
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
        <TableData>{{ count[5] * 5 }}</TableData>
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
        <TableData>{{ count[6] * 6 }}</TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
      </TableRow>
      <TableRowSpan>
        <TableData colspan="2">
          <div class="flex justify-between">
            <p>Total Points</p>
            <i class="fas fa-arrow-right" style="font-size: 24px"></i>
          </div>
        </TableData>
        <TableData>{{ numScoreTotal }}</TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
      </TableRowSpan>
      <TableRow>
        <TableData>
          <div class="flex justify-between">
            <p>Bonus</p>
            <p class="text-xs text-center">
              if more than<br />
              63 points
            </p>
          </div>
        </TableData>
        <TableData>35 Points</TableData>
        <TableData>{{ bonusScore }}</TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
      </TableRow>
      <TableRowSpan>
        <TableData colspan="2">
          <div class="flex justify-between">
            <p>Total Points of Part One</p>
            <i class="fas fa-arrow-right" style="font-size: 24px"></i>
          </div>
        </TableData>
        <TableData>{{ numScoreTotal + bonusScore }}</TableData>
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
        <TableData class="w-1/12">{{ threeKind }}</TableData>
        <TableData class="w-1/12"></TableData>
        <TableData class="w-1/12"></TableData>
        <TableData class="w-1/12"></TableData>
        <TableData class="w-1/12"></TableData>
      </TableRow>
      <TableRow>
        <TableData>Four of a Kind</TableData>
        <TableData>Total of Dice</TableData>
        <TableData>{{ fourKind }}</TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
      </TableRow>
      <TableRow>
        <TableData>Full House</TableData>
        <TableData>25 Points</TableData>
        <TableData>{{ fullHouse }}</TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
      </TableRow>
      <TableRow>
        <TableData>
          <div class="flex justify-between">
            <p>Small Straight</p>
            <p class="text-xs text-center">Sequence<br />of 4 dice</p>
          </div>
        </TableData>
        <TableData>30 Points</TableData>
        <TableData>{{ smallStraight }}</TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
      </TableRow>
      <TableRow>
        <TableData>
          <div class="flex justify-between">
            <p>Large Straight</p>
            <p class="text-xs text-center">Sequence<br />of 5 dice</p>
          </div>
        </TableData>
        <TableData>40 Points</TableData>
        <TableData>{{ largeStraight }}</TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
      </TableRow>
      <TableRow>
        <TableData>
          <div class="flex justify-between">
            <p>Yahtzee</p>
            <p class="text-xs text-center">5 of a<br />kind</p>
          </div>
        </TableData>
        <TableData>50 Points</TableData>
        <TableData>{{ yahtzee }}</TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
      </TableRow>
      <TableRow>
        <TableData>Chance</TableData>
        <TableData>Total of Dice</TableData>
        <TableData>{{ chance }}</TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
      </TableRow>
      <TableRowSpan>
        <TableData colspan="2">
          <div class="flex justify-between">
            <p>Total Points of Part Two</p>
            <i class="fas fa-arrow-right" style="font-size: 24px"></i>
          </div>
        </TableData>
        <TableData>{{ bottomScore }}</TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
      </TableRowSpan>
      <TableRowSpan>
        <TableData colspan="2">
          <div class="flex justify-between">
            <p>Total Points of Part One</p>
            <i class="fas fa-arrow-right" style="font-size: 24px"></i>
          </div>
        </TableData>
        <TableData>{{ numScoreTotal + bonusScore }}</TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
      </TableRowSpan>
      <TableRowSpan>
        <TableData colspan="2">
          <div class="flex justify-between">
            <p class="font-bold">Total Score</p>
            <i class="fas fa-arrow-right" style="font-size: 24px"></i>
          </div>
        </TableData>
        <TableData>{{ numScoreTotal + bonusScore + bottomScore }}</TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
        <TableData></TableData>
      </TableRowSpan>
    </tbody>
  </table>
</template>
