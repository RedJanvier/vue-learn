<template>
  <div>
    <ul class="robots-list">
      <li v-bind:key="robot.id" v-for="robot in robots" >
        <Robot v-bind:robot="robot" />
      </li>
    </ul>
  </div>
</template>

<script>
import Robot from './Robot.vue';

export default {
  name: 'Robots',
  components: {
    Robot
  },
  props: {
    robots: Array
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
.robots-list {
  display: flex;
  flex-flow: row wrap;
  justify-content: center;
  align-items: center;
  max-height: 530px;
  overflow: scroll;
}
li {
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
