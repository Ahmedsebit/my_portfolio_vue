<template>
  <div class="main">
    <b-navbar toggleable type="inverse">

    <b-nav-toggle target="nav_collapse"></b-nav-toggle>

    <b-link class="navbar-brand" to="#">
      <span>My Portfolio</span>
    </b-link>

    <b-collapse is-nav id="nav_collapse">
      
      <b-nav is-nav-bar>
        <b-nav-item>About Me</b-nav-item>
        <b-nav-item>My Portfolio</b-nav-item>
        <b-nav-item>Contact Me</b-nav-item>
      </b-nav>
      
      <b-nav is-nav-bar class="ml-auto">
        
          <!-- Navbar dropdowns -->
          <b-nav-item-dropdown text="Lang" right>
            <b-dropdown-item to="#">EN</b-dropdown-item>
            <b-dropdown-item to="#">ES</b-dropdown-item>
            <b-dropdown-item to="#">RU</b-dropdown-item>
            <b-dropdown-item to="#">FA</b-dropdown-item>
          </b-nav-item-dropdown> 
        </b-nav>
      </b-collapse>
    </b-navbar>
    <b-jumbotron header="Ahmed Yusuf"
                 lead="Automation Engineer" 
                 height="500px"
                 img="https://s-media-cache-ak0.pinimg.com/originals/c3/51/ab/c351ab4b9db84d85a8d4f2796c32caba.jpg">
        <p>For more information visit website</p>
        <b-btn style="background-color:#282E2B; color:#FFF" href="#">My Portfolio</b-btn>
    </b-jumbotron>

  <h1>About Me</h1>

  <div class="row">
  <div class="col-1"></div>  
  <div class="col-5">
    <b-card title="Who I'm I?" class="mb-2 about">
        Andela provides companies with access to the top 1% of global tech talent. 
        We identify high-potential developers on the African continent, 
        shape them into world-class technical leaders, and pair them with companies as 
        full-time, distributed team members. This allows Andela's partners, which range 
        from startups to Fortune 500s, to accelerate their product roadmaps while minimizing 
        time spent interviewing, on-boarding, and training new hires.
        
        Andela is backed by investors including Spark Capital, Omidyar Network, 
        Susa Ventures, Steve Case, Founder Collective, Rothenberg Ventures, Learn Capital and 
        more
    </b-card>
  </div>

  <div class="col-6">
    <b-card title="Skills" class=" mb-2 about">
      <p>Backedend Development
      <b-progress v-model="backend_counter" :precision="1" show-progress animated></b-progress></p>
      <p>Frontend Development
      <b-progress v-model="frontend_counter" :precision="1" show-progress animated></b-progress></p>
      <p>Machine Learning
      <b-progress v-model="machinelearning_counter" :precision="1" show-progress animated></b-progress></p>
      <p>Data Science
      <b-progress v-model="datascience_counter" :precision="1" show-progress animated></b-progress></p>
      <p>For more infomation on skills, click to download my cv</p>
      
    </b-card>
  </div>
  </div>
  <div class="rule"></div>
  <hr class="half-rule rule">
  <h1 class="page-header">My Portfolio</h1>
  <div class="row">
    <div class="col-4 transform_portfolio_1">
    </div>
    <div class="col-4 transform_portfolio_2">
    </div>
    <div class="col-4 transform_portfolio_1">
    </div> 
  </div>

  <div class="rule"></div>
  <h1 class="page-header">Contact Me</h1>
  <div class="row">
    <div class="col-1"></div>
    <div class="col-5">
      <h1 class="contact-header">Hire Me</h1>
      <p>I am seeking a contracts on automation projects
        which deal with artificial inteligence, machine leaning,
        data mining and fullstack development. I'm seeking
        new challenges and the opportunity to work along with talented people.
      </p>
      <div class="row">
        <div class="col-3"></div>
      <div class="col-2">
        <icon name="facebook" scale="2"></icon>
      </div>
      <div class="col-2">
        <icon name="twitter" scale="2"></icon>
      </div>
      <div class="col-2">
        <p><icon name="google-plus" scale="2"></icon></p>
      </div>
      <div class="col-3"></div>
      </div>
    </div>
    <div class="col-5">
      <b-card title="Reach Out" class=" mb-2">
        <p><b-form-input v-model="text" type="text" placeholder="Enter your email"></b-form-input></p>

        <p><b-form-input v-model="text" type="text" placeholder="Enter your name"></b-form-input></p>

        <p><b-form-input v-model="text" type="text" placeholder="Enter your phonenumber"></b-form-input></p>

        <p><b-form-input textarea v-model="text" placeholder="Typt your message here"></b-form-input></p>
        <p><b-btn style="background-color:#4F5C56; color:#FFF" href="#">Send</b-btn></p>
      </b-card>

    </div>
    <div class="col-1"></div>
  </div>
  <div class="rule"></div>
  <hr class="half-rule rule">
  <div class="footer">© 2017 Ahmed Yusuf - All Rights Reserved.</div>
  </div>
  
</template>

<script>
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'

export default {
  name: 'main',
  data () {
    return {
      heading: 'Software developement with a midas touch',
      backend_counter: 100,
      frontend_counter: 90,
      machinelearning_counter: 45,
      datascience_counter: 45,
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

.about{
  width: 500px
}

.transform_portfolio_1 {
    height: 600px;
    background-color: #4F5C56;
}

.transform_portfolio_1:hover {
    height: 600px;
    background-color: #282E2B;
}

.transform_portfolio_2 {
    height: 600px;
    background-color: #282E2B;
}

.transform_portfolio_2:hover {
    height: 600px;
    background-color: #4F5C56;
}

.rule{
  padding-top: 20px;
  padding-bottom: 20px;
}

.contact-header{
  font-size:5.5em;
}

.fa-icon {
  width: auto;
  height: 3em; /* or any other relative font sizes */
}

.footer{
  padding-bottom: 20px;
}
</style>
