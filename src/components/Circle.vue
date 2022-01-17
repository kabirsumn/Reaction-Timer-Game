<template>
  <div v-show="showCircle" class="circle">click here</div>
</template>

<script>
export default {
  props: ['delay'],

  data() {
    return {
      showCircle: false,
    };
  },

  mounted() {
    setTimeout(() => {
      this.showCircle = true;
    }, this.delay);
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
