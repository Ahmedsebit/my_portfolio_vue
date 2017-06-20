<template>
  <div class="main">
    <ul class="topnav">
      <li><a class="active" href="#home">Home</a></li>
      <li><a href="#news">What I do</a></li>
      <li><a href="#contact">My Work</a></li>
      <li class="right"><a href="#about">About Me</a></li>
    </ul>
    <div class="app_main">
      <div class="app_content">
      <h1>{{ heading }}</h1>
      <div class="quotes_heading"></div>
      <div class="quotes">
        <carousel>
          <slide>
            Slide 1 Content
          </slide>
          <slide>
            Slide 2 Content
          </slide>
      </carousel>
      </div>
      </div>
    </div>

    <div class="app_work">
      <div class="app_content"> <h1> What I do</h1> </div>
    </div>

    <div class="app_portfolio">
      <div class="app_content"> <h1> Portfolio</h1> </div>
    </div>

    <div class="app_contact">
      <div class="app_content"> <h1> Contacts</h1> </div>
    </div>

    <div class="app_footer">
      
    </div>
    
  </div>
</template>

<script>
import { Carousel, Slide } from 'vue-carousel'

export default {
  name: 'main',
  components: {
    Carousel,
    Slide
  },
  data () {
    return {
      heading: 'Software developement with a midas touch',
      name: {
        firstName: 'Ahmed',
        secondName: 'Yusuf'
      },
      messages: [
        {title: ' ', msg: 'Deligent', author: 'Customer One', company: 'Company One'},
        {title: ' ', msg: 'World class', author: 'Customer Two', company: 'Company Two'},
        {title: ' ', msg: 'Attention to details', author: 'Customer Three', company: 'Company Three'}
      ],
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

h1 {
	font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
	font-size: 24px;
	font-style: normal;
	font-variant: normal;
	font-weight: 500;
	line-height: 26.4px;
}

h3 {
	font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
	font-size: 14px;
	font-style: normal;
	font-variant: normal;
	font-weight: 500;
	line-height: 15.4px;
}

p {
	font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
	font-size: 14px;
	font-style: normal;
	font-variant: normal;
	font-weight: 400;
	line-height: 20px;
}

blockquote {
	font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
	font-size: 21px;
	font-style: normal;
	font-variant: normal;
	font-weight: 400;
	line-height: 30px;
}

pre {
	font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
	font-size: 13px;
	font-style: normal;
	font-variant: normal;
	font-weight: 400;
	line-height: 18.5714px;
}

.name{
    color: #FEFEFF;
    padding-left: 10px;
    padding-top:10px;
    font-size: 1.2em;
    text-align: left;
}

ul.topnav li {float: left;}

ul.topnav li a {
    display: block;
    color: white;
    text-align: center;
    padding: 24px 16px;
    text-decoration: none;
}

ul.topnav {
    list-style-type: none;
    margin: 0;
    padding: 0;
    overflow: hidden;
    background-color: #376873;
}

ul.topnav li a:hover:not(.active) {background-color: #78E3FD;}

ul.topnav li a.active {background-color: #78E3FD;}

ul.topnav li.right {float: right;}

@media screen and (max-width: 600px){
    ul.topnav li.right, 
    ul.topnav li {float: none;}
}

.quotes_heading{
  width: 400px;
  height: 50px;
  margin-left: 50px;
  margin-top: 100px;
  background-color: #376873;
}

.quotes{
  width: 400px;
  height: 200px;
  margin-left: 50px;
  background-color: #78E3FD;
}

.app_content{
  width: 100%;
  padding-top: 10px;
}

.app_main{
  background-color: #FEFEFF;
  width:100%;
  height:600px;
  color: #376873;
}

.app-heading{
  font-family: Helvetica;
}

.app_work{
  background-color: #78E3FD;
  width:100%;
  height:300px;
  color: #376873;
}

.app_portfolio{
  background-color: #376873;
  width:100%;
  height:600px;
  color: #FEFEFF;
}

.app_contact{
  background-color: #78E3FD;
  width:100%;
  height:600px;
}

.app_footer{
  background-color: #376873;
  width:100%;
  height:50px;
}

</style>
