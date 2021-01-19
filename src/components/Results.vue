 <template>
  <div>
    <p>Your result: {{score}} ms</p>
    <p class="rank">{{rank}}</p>
  </div>
</template>

<script>
export default {
  props: ['score'],
  data() {
    return {
      rank: null
    }
  },
  mounted() {
    if(this.score < 250) {
      this.rank = 'Amazing speed'
    } else if (this.score < 500) {
      this.rank = 'Not bad speed'
    } else {
      this.rank = 'Are you a snail?'
    }
  }
}
</script>

<style>
  .rank {
    font-size: 1.4em;
    color: #0faf87;
    font-weight: bold
  }
</style>