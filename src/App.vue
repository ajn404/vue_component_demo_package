<template>
  <div>
    <span ref="countup"></span>
  </div>
</template>

<script>
import CountUp from "countup.js";
export default {
  name: "countup-demo",
  props: {
    start: {
      type: Number,
      default: 0
    },
    end: {
      type: Number,
      default: 2017
    },
    decimal: {
      type: Number,
      default: 0
    },
    duration: {
      type: Number,
      default: 2.5
    },
    options: {
      type: Object
    },
    autoplay: {
     type: Boolean,
     required: false,
     default: true
   }
  },
  data() {
    return {
      numAnim: null,
      another: null
    };
  },
  mounted() {
    this.initCountUp();
  },
  methods: {
    initCountUp() {
      this.numAnim = new CountUp(
        this.$refs.countup,
        this.start,
        this.end,
        this.decimal,
        this.duration,
        this.options
      );
      if(this.autoplay)
      this.numAnim.start();
    }
  }
};
</script>
