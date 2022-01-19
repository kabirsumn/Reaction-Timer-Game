<template>
  <div v-show="showCircle" class="circle" @click="stopTimer">click here</div>
</template>

<script>
export default {
  props: ['delay'],

  data() {
    return {
      showCircle: false,
      timer: null,
      reactionTime: 0,
    };
  },

  mounted() {
    setTimeout(() => {
      this.showCircle = true;
      this.startTimer();
    }, this.delay);
  },

  methods: {
    startTimer() {
      this.timer = setInterval(() => {
        this.reactionTime += 10;
      }, 10);
    },
    stopTimer() {
      clearInterval(this.timer);
      console.log(this.reactionTime);
    },
  },
};
</script>

<style>
.circle {
  margin: 1.75rem auto;
  padding: 75px 0;
  width: 150px;
  background-color: #a0f750;
  border-radius: 50%;
}
</style>
