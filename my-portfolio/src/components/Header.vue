<template>
  <div class="main">
      <nav></nav>   
      <h1>{{ heading }}</h1>
  </div>
</template>

<script>
export default {
  name: 'main',
  data () {
    return {
      heading: 'Welcome to My Portfolio Page',
      name: {
        firstName: 'Ahmed',
        secondName: 'Yusuf'
      },
      contacts: {
        phone: '+2450701874389',
        email: 'ahmed.yusuf@andela.com'
      },
      work: [
        {title: 'item one'},
        {title: 'item two'},
        {title: 'item three'}
      ]
    }
  },
  methods: {
    greet: function (greeting) {
      alert(greeting)
    }
  },
  computed: {
    fullName: function () {
      return this.firstName + ' ' + this.secondName
    }
  }
}
</script>


<style scoped>
h1, h2 {
  font-weight: normal;
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
