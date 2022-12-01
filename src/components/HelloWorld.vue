<template>
  <div class="hello">
    <h1>{{ hello }}</h1>

    <h2 v-if="isClicMode"> We change to click mode: {{ clicks }}</h2>

    <button @click="clickMe()">ClickMe</button>

  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';

@Options({
  props: {
    msg: String
  }
})
export default class HelloWorld extends Vue {
  msg!: string
  hello: string = this.msg;
  clicks = 0;

  clickMe(): void {
    this.hello = 'Hello my friend';
    this.clicks += 1;
  }

  mounted() {
    console.log('Im on mounted')
  }

  get isClicMode(): boolean {
    return this.clicks > 0;
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
