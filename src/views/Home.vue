<template>
  <div>
    <SearchRobots v-on:search-robots="searchRobots"/>
    <Robots v-bind:robots="searchedRobots"/>
  </div>
</template>

<script>
import Robots from '../components/Robots.vue';
import SearchRobots from '../components/SearchRobots';

export default {
  name: 'App',
  components: {
    Robots,
    SearchRobots
  },
  methods: {
    searchRobots(input) {
      return this.searchedRobots = this.robots.filter(robot => robot.name.toLowerCase().includes(input));
    }
  },
  created() {
    fetch('http://jsonplaceholder.typicode.com/users')
      .then(res => res.json())
      .then(data => {
        this.robots = data;
        return this.searchedRobots = this.robots;
      })
      .catch(console.log);
  },
  data() {
    return {
      robots: [],
      searchedRobots: []
    }
  }
}
</script>

<style>
</style>
