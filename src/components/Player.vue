<template>
  <div id="player">
    <div id="player-hand">
      <div id="player-card-sum">
        {{ cardSumMessage }}
      </div>
    </div>
    <div id="betting-box">
      <p id="bet">{{ betMessage }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Player',

  data() {
    return {
      hand: [15],
      bet: null,
    }
  },

  computed: {
    cardSumMessage() {
      if (!this.hand.length) {
        return ''
      } else {
        return '' + this.hand.reduce((sum, card) => sum+card, 0)
      }
    },

    betMessage() {
      if (this. bet) {
        return `${this.bet}K`
      } else {
        return 'NO BET.'
      }
    },
  }

}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,300;0,400;0,500;0,600;0,700;1,300;1,400;1,500;1,600;1,700&display=swap');

#player {
  width: 100%;
}

#player-hand {
  height: 100px;
  border: solid black 5px;
  border-radius: 20px;
  display: flex;
  justify-content: start;
}
#betting-box {
  height: 50px;
  margin: 20px;
  border: solid black 5px;
  border-radius: 20px;
}

#bet {
  text-align: center;
  margin: 7px;
  font-family: 'Montserrat', sans-serif;
  font-size: 30px;
  font-weight: 600;
}

#player-card-sum {
  text-align: center;
  margin-left: auto;
  font-family: 'Montserrat', sans-serif;
  font-size: 30px;
  font-weight: 600;
  width: 50px;
  /* position: absolute; */
}

</style>