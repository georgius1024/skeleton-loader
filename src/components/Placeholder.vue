<template>
  <div class="placeholder" :class="placeholderClass" />
</template>
<script>
export default {
  name: "Placeholder",
  props: {
    type: {
      type: String,
      default: "text",
      validator: (value) => ["text", "header", "button", "avatar", "picture"].includes(value),
    },
  },
  computed: {
    placeholderClass() {
      return `placeholder-${this.type}`;
    },
  },
};
</script>
<style lang="scss">
.placeholder {
  background: rgb(204, 204, 204);
  position: relative;
  overflow: hidden;
  &:after {
    content: "";
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    position: absolute;
    // transform: translateX(-100%);
    background: linear-gradient(
      90deg,
      rgba(204, 204, 204, 1) 0%,
      rgba(151, 151, 151, 0.3) 50%,
      rgba(204, 204, 204, 1) 100%
    );
    animation: placeholder-loading-animation linear 1.5s infinite;
  }
  &.placeholder-text {
    height: 24px;
    display: block;
    border-radius: 100px;
    margin: 0 18px 18px 0;
  }
  &.placeholder-header {
    height: 48px;
    display: block;
    border-radius: 100px;
    margin: 0 0 18px 0;
  }
  &.placeholder-button {
    height: 48px;
    width: 200px;
    display: block;
    border-radius: 2px;
    margin: 0 18px 18px 0;
  }
  &.placeholder-avatar {
    height: 48px;
    width: 48px;
    display: block;
    border-radius: 100%;
    margin: 0 18px 18px 0;
  }
  &.placeholder-picture {
    display: block;
    border-radius: 0;
    margin: 0 18px 18px 0;
  }

}

@keyframes placeholder-loading-animation {
  // 0% {
  //   transform: translate3d(-100%);
  // }
  // 100% {
  //   transform: translate3d(100%);
  // }
  0% {
    transform: translateX(-100%);
  }
  100% {
    transform: translateX(100%);
  }
}
</style>
