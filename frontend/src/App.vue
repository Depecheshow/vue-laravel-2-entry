<template>
  <div id="app">
      {{ some }}
  </div>
</template>

<script>
import axios from 'axios'

export default {
    data: function () {
      return {
          some: null,
      }
    },
  name: 'App',
    created() {
      axios.get('/api/some')
        .then(res => this.some = res.data)
    }
}
</script>

<style>
</style>
