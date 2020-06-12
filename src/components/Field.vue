<template>
  <div>
    <h1>{{ msg }}</h1>
    <input type="text" :value="msg" @input="changeMess"/>
    <br>
    {{ message }}
  </div>
</template>

<script>
//v-model="message"
  export default {
    data() {
      return {
        message: ''
      }
    },
    methods: {
      changeMess(event) {
        this.message = event.target.value;
        this.$emit('messChange', this.message);
      }
    },
    props: ['msg']
  }
</script>