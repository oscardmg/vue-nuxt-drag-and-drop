<template>
  <v-layout
    column
    justify-center
    align-center
  >
    <main class="flexbox">
      <board id="board-1">
        <card v-for="card in cards" :key="card.id" :id="'card' + card.id" draggable="true">
          <p>Card {{ card.id }}</p>
        </card>
      </board>

      <board id="board-2">
        <card v-for="card in cards1" :key="card.id" :id="'card' + card.id" draggable="true">
          <p>Card {{ card.id }}</p>
        </card>
      </board>
    </main>
    <board />
  </v-layout>
</template>

<script>
import Board from '@/components/Board';
import Card from '@/components/Card';

export default {
  components: {
    Board, Card
  },
  data () {
    return {
      cards: [
        { id: 'one' },
        { id: 'two' },
        { id: 'three' }
      ],
      cards1: [
        { id: 'four' },
        { id: 'five' },
        { id: 'six' }
      ]
    };
  }
};
</script>
