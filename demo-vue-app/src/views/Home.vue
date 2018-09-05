<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <Example msg="Welcome to Your Vue.js + TypeScript App"/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import Example from '@/components/ExampleComponent.vue'; // @ is an alias to /src

@Component({
  components: {
    Example,
  },
})
export default class Home extends Vue {}
</script>
