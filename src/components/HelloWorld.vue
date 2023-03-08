<template>
  <div>
    <p>
      Lorem ipsum dolor, sit amet consectetur adipisicing elit. Molestias nihil aliquam expedita asperiores ullam cumque nam, odio ab nisi aperiam dolorem vel aliquid error impedit! Veritatis quidem optio dolore incidunt?
    </p>
    <p>{{ msg }}</p>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
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
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
