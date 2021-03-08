<template>
  <div class="row">
    <div style="min-width: 340px">
      <Placeholder type="header" />
    </div>
    <div class="col"></div>
  </div>
  <div class="row">
    <div class="col">
      <Placeholder />
    </div>
    <div class="col">
      <Placeholder />
    </div>
    <div class="col">
      <Placeholder />
    </div>
  </div>
  <div class="row">
    <div>
      <Placeholder type="avatar"/>
    </div>
    <div class="col">
      <Placeholder />
    </div>
    <div class="col">
      <Placeholder />
    </div>
  </div>
  <div class="row">
    <div class="col"></div>
    <div style="min-width: 140px">
      <Placeholder type="button" />
    </div>
    <div style="min-width: 140px">
      <Placeholder type="button" />
    </div>
  </div>

</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
//
import Placeholder from "./components/Placeholder.vue";
export default {
  name: "App",
  components: {
    HelloWorld,
    Placeholder,
  },
};

// This starter template is using Vue 3 experimental <script setup> SFCs
// Check out https://github.com/vuejs/rfcs/blob/script-setup-2/active-rfcs/0000-script-setup.md
</script>
<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.row {
  display: flex;
  align-items: center;
  flex-direction: row;
  .col {
    flex-grow: 1;
  }
}
</style>
