<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorldContainer />
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import HelloWorldContainer from '@/containers/HelloWorldContainer.vue'; // @ is an alias to /src

@Options({
  components: {
    HelloWorldContainer,
  },
})
export default class Home extends Vue {}
</script>
