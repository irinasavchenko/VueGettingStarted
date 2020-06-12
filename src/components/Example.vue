<template>
  <div>
    <h1>Text Example</h1>
    <app-input :msg="message" @messChange = "message = $event"></app-input>
  </div>
</template>

<script>

import Input from './Field';

export default {
  data() {
    return {
      message: 'New message'
    }
  },
  components: {
    'app-input': Input
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>