<template>
    <div>
      <h3>{{ copyright }}</h3>
    </div>
</template>

<script>
export default {
  name: 'ponzfooter',
  data () {
    return {
      copyright: '© 2021 Ponzliquid'
    }
  },
  methods: {
  }
}
</script>

<style scoped>
h1{
  display: center;
  font-weight: normal;
  font-size: xx-large;
}
h2{
  font-weight: normal;
  font-size: large;
  margin-bottom: 20px;
}
h3{
  font-weight: normal;
  font-size: small;
  /* margin-bottom: 0px; */
  color: #696773;
}
</style>
