<template>
  <input type="text" placeholder="Search Robots..." name="search_text" v-model="searchText" @input="handleSearch">
</template>

<script>
export default {
    data() {
        return {
            searchText: ''
        }
    },
    methods: {
        handleSearch(){
            return this.$emit('search-robots', this.searchText.toLowerCase().trim())
        }
    }
}
</script>

<style>

</style>