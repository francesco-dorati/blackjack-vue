<template>
  <div id="table">
    <Dealer/>
    <!-- <Player/> -->
    <Player/>
  </div>
</template>

<script>
import Dealer from './Dealer.vue'
import Player from './Player.vue'

export default {
  name: 'Game',

  components: {
    Dealer,
    Player
  }
}
</script>

<style>
#table {
  margin: 15%;
  /* display: flex;
  flex-direction: column;
  justify-content: space-between; */
}
#player {
  margin-top: 200px;
}


</style>