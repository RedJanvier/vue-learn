<template>
  <div class="robot">
      <img :src="'http://robohash.org/' + robot.id + '?size=200x200'"/>
      <h2>{{robot.name}}</h2>
      <p>{{robot.email}}</p>
  </div>
</template>

<script>
export default {
    name: 'Robot',
    props: {
        robot: Object
    }
}
</script>

<style scoped>
    .robot {
        border: 2px solid rgb(33, 190, 138);
        padding: 2rem;
        margin: .6rem 0;
        width: 210px;
        height: 250px;
        border-radius: 6px;
        transition: all .1s ease-in-out;
    }
    .robot:hover {
        position: relative;
        font-size: 17px;
        box-shadow: 1px 1px 6px #666;
    }
    .robot h2 {
        margin: .2rem;
        font-size: 18px;
    }
    .robot p {
        margin: .2rem;
    }
</style>