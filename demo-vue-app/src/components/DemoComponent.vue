<template>
  <div class="hello">
    <h2>This is an application developed using vue.js</h2>
    <p>{{message}}</p>
    <div class="content">
      <b>Tell us your opinion about Vue:</b>
      <br/><br/>
      {{comment}}
      <br/><br/>
      <button @click="generateOpinion">Generate opinion</button>
      <br/><br/><br/>
      <input type="text" v-model="comment" />
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component({})
export default class Demo extends Vue {
  public message: string = "Vue is very easy to learn!";
  public comment: string = "Generic comment";

  public mounted() {}

  public generateOpinion(): void {
    let opinions = [
      "Great!",
      "Very easy to learn!",
      "Amazing!",
      "Exciting!",
      "Fantastic!",
      "Superb!",
      "I love it!"
    ];
    this.comment = opinions[Math.floor(Math.random() * opinions.length)];
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

.content{
  margin-top: 45px;
  font-size: 20px;  
}
</style>
