<template>
  <div class="room">
    <h1>Room: {{ slug }}</h1>
    <hr />

    <div class="board">
      <board-card v-for="card in board.cards" :key="card.word" :card="card" />
    </div>
  </div>
</template>

<script>
import words from '@/mock/words'
import BoardCard from '../components/boardCard'

const getRandomIndex = limit => Math.floor(Math.random() * (limit + 1))

const generateBoard = () => {
  const board = {}
  board.cards = []

  for (let i = 0; i < 25; ++i) {
    board.cards.push({
      word: words[getRandomIndex(words.length)]
    })
  }
  return board
}

export default {
  props: {
    slug: {
      type: String
    }
  },
  data () {
    return {
      board: generateBoard()
    }
  },
  created () {
    // TODO fetch game data
  },
  components: {
    BoardCard
  }
}
</script>

<style scoped lang="less">
.board {
  display: flex;
  flex-wrap: wrap;

  > * {
    width: 20%;
  }
}
</style>
