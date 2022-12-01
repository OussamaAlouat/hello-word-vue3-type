<template>
  <div class="hello">
    <h1>{{ hello }}</h1>

    <button @click="sayHello()">ClickMe</button>
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

  sayHello(): void {
    console.log('Hello');
    this.hello = 'Hello my friend';
  }

  mounted() {
    console.log('Im on mounted')
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
