<template>
<div class="home flex-grow-1 d-flex flex-column align-items-center justify-content-center">
  <img src="../assets/img/cw-circle.png" alt="CodeWorks Logo">
  <h1>Welcome {{ user.name }}</h1>
  <Experimental>
    <div>Features!</div>
    <Experimental />
</div>
</template>

<script>
import {
  computed
} from "vue"
import {
  AppState
} from "../AppState"
export default {
  name: 'Home',
  setup() {
    return {
      user: computed(() => AppState.user)
    }
  }
}
</script>

<style lang="scss" scoped>
.home {
  text-align: center;

  img {
    height: 250px;
    width: 250px;
  }
}
</style>
