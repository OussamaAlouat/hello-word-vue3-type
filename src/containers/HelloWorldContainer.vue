<template>
  <div>
    <HelloWorld :msg="msg"/>
  </div>
</template>

<script lang="ts">

import { Options, Vue } from 'vue-class-component';
import HelloWorld from '@/components/HelloWorld.vue'; // @ is an alias to /src

@Options({
  components: {
    HelloWorld
  }
})
export default class HelloWorldContainer extends Vue {
  msg = 'Hello  word';
}
</script>

