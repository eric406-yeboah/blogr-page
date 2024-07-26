<template>
  <div id="app">
    <!-- Header starts here -->
    <header class="header">
      <div class="nav ">
        <a href="#"><img src="/images/logo.svg" ></a>
        <ul class="top">
          <li>
            <a href="#">Product</a>
            <img src="/images/icon-arrow-light.svg" alt="dropdown arrow" @click="toggleDropdown('product')">
            <div class="drop" v-if="dropdowns.product">
              <ul>
                <li><a href="#">Overview</a></li>
                <li><a href="#">Pricing</a></li>
                <li><a href="#">Marketplace</a></li>
                <li><a href="#">Features</a></li>
                <li><a href="#">Integrations</a></li>
              </ul>
            </div>
          </li>
          <li>
            <a href="#">Company</a>
            <img src="/images/icon-arrow-light.svg" alt="dropdown arrow" @click="toggleDropdown('company')">
            <div class="drop" v-if="dropdowns.company">
              <ul>
                <li><a href="#">About</a></li>
                <li><a href="#">Team</a></li>
                <li><a href="#">Blog</a></li>
                <li><a href="#">Careers</a></li>
              </ul>
            </div>
          </li>
          <li>
            <a href="#">Connect</a>
            <img src="/images/icon-arrow-light.svg" alt="dropdown arrow" @click="toggleDropdown('connect')">
            <div class="drop" v-if="dropdowns.connect">
              <ul>
                <li><a href="#">Contact</a></li>
                <li><a href="#">Newsletter</a></li>
                <li><a href="#">LinkedIn</a></li>
              </ul>
            </div>
          </li>
        </ul>
        <ul class="registeration">
          <li><a href="#" class="login">Login</a></li>
          <li><a href="#" class="signup">Sign Up</a></li>
        </ul>
        <img src="/images/icon-hamburger.svg" alt="hamburger" id="mobilemenu" @click="toggleMobileMenu">
      </div>

      <div class="header-content">
        <h1>A modern publishing platform</h1>
        <p>Grow your audience and build your online brand</p>
        <ul class="header-content-links">
          <li><a href="#" class="start">Start for free</a></li>
          <li><a href="#" class="learn">Learn More</a></li>
        </ul>
      </div>
    </header>

    <!-- Mobile Navigation starts here -->
    <div id="mobilenav" class="mobilenav" v-if="mobileMenu">
      <ul>
        <li class="connect">
          <div class="connect-text">
            <a href="#">Product</a>
            <img src="/images/icon-arrow-dark.svg" alt="dropdown arrow" @click="toggleDropdown('productMobile')">
          </div>
          <div class="drop-mobile" v-if="dropdowns.productMobile">
            <ul>
              <li><a href="#">Overview</a></li>
              <li><a href="#">Pricing</a></li>
              <li><a href="#">Marketplace</a></li>
              <li><a href="#">Features</a></li>
              <li><a href="#">Integrations</a></li>
            </ul>
          </div>
        </li>
        <li class="connect">
          <div class="connect-text">
            <a href="#">Company</a>
            <img src="/images/icon-arrow-dark.svg" alt="dropdown arrow" @click="toggleDropdown('companyMobile')">
          </div>
          <div class="drop-mobile" v-if="dropdowns.companyMobile">
            <ul>
              <li><a href="#">About</a></li>
              <li><a href="#">Team</a></li>
              <li><a href="#">Blog</a></li>
              <li><a href="#">Careers</a></li>
            </ul>
          </div>
        </li>
        <li class="connect">
          <div class="connect-text">
            <a href="#">Connect</a>
            <img src="/images/icon-arrow-dark.svg" alt="dropdown arrow" @click="toggleDropdown('connectMobile')">
          </div>
          <div class="drop-mobile" v-if="dropdowns.connectMobile">
            <ul>
              <li><a href="#">Contact</a></li>
              <li><a href="#">Newsletter</a></li>
              <li><a href="#">LinkedIn</a></li>
            </ul>
          </div>
        </li>
        <li><a href="#">Login</a></li>
        <li class="signup"><a href="#">Sign Up</a></li>
      </ul>
    </div>

    <!-- Blogr description -->
    <section class="description">
      <h2 class="move">Designed for the future</h2>
      <div class="description-content">
        <div class="description-content-leftcolumn">
          <h3>Introducing an extensible editor</h3>
          <p>
            Blogr features an exceedingly intuitive interface which lets you focus on one thing: creating content.
            The editor supports management of multiple blogs and allows easy manipulation of embeds such as images,
            videos, and Markdown. Extensibility with plugins and themes provide easy ways to add functionality or
            change the looks of a blog.
          </p>
          <h3>Robust content management</h3>
          <p>
            Flexible content management enables users to easily move through posts. Increase the usability of your blog
            by adding customized categories, sections, format, or flow. With this functionality, you’re in full control.
          </p>
        </div>
        <div class="description-content-rightcolumn">
          <img src="/images/illustration-editor-desktop.svg" alt="editor illustration" class="desktop-editor">
          <img src="/images/illustration-editor-mobile.svg" alt="editor illustration" class="mobile-editor">
        </div>
      </div>
    </section>

    <!-- Services -->
    <section class="services">
      <div class="services-leftcolumn">
        <img src="/images/illustration-phones.svg" alt="phone illustration" class="phone">
        <img src="/images/bg-pattern-circles.svg" alt="circle pattern" class="circle-pattern">
      </div>
      <div class="services-rightcolumn">
        <h4>State of the Art Infrastructure</h4>
        <p>
          With reliability and speed in mind, worldwide data centers provide the backbone for ultra-fast connectivity.
          This ensures your site will load instantly, no matter where your readers are, keeping your site competitive.
        </p>
      </div>
    </section>

    <!-- Features -->
    <section class="features">
      <div class="features-leftcolumn">
        <img src="/images/illustration-laptop-desktop.svg" alt="laptop illustration" class="desktop-illustration">
        <img src="/images/illustration-laptop-mobile.svg" alt="laptop illustration" class="mobile-illustration">
      </div>
      <div class="features-rightcolumn">
        <h5>Free, open, simple</h5>
        <p>
          Blogr is a free and open source application backed by a large community of helpful developers. It supports
          features such as code syntax highlighting, RSS feeds, social media integration, third-party commenting tools,
          and works seamlessly with Google Analytics. The architecture is clean and is relatively easy to learn.
        </p>
        <h5>Powerful tooling</h5>
        <p>
          Batteries included. We built a simple and straightforward CLI tool that makes customization and deployment a breeze, but
          capable of producing even the most complicated sites.
        </p>
      </div>
    </section>

    <!-- Footer -->
    <footer>
      <div class="down">
        <a href="#"><img src="/images/logo.svg" alt="Blogr logo"></a>
      </div>
      <div class="down">
        <h6>Product</h6>
        <ul>
          <li><a href="#">Overview</a></li>
          <li><a href="#">Pricing</a></li>
          <li><a href="#">Marketplace</a></li>
          <li><a href="#">Features</a></li>
          <li><a href="#">Integrations</a></li>
        </ul>
      </div>
      <div class="down">
        <h6>Company</h6>
        <ul>
          <li><a href="#">About</a></li>
          <li><a href="#">Team</a></li>
          <li><a href="#">Blog</a></li>
          <li><a href="#">Careers</a></li>
        </ul>
      </div>
      <div class="down">
        <h6>Connect</h6>
        <ul>
          <li><a href="#">Contact</a></li>
          <li><a href="#">Newsletter</a></li>
          <li><a href="#">LinkedIn</a></li>
        </ul>
      </div>

    </footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      dropdowns: {
        product: false,
        company: false,
        connect: false,
        productMobile: false,
        companyMobile: false,
        connectMobile: false,
      },
      mobileMenu: false
    };
  },
  methods: {
    toggleDropdown(menu) {
      this.$set(this.dropdowns, menu, !this.dropdowns[menu]);
    },
    toggleMobileMenu() {
      this.mobileMenu = !this.mobileMenu;
    }
  }
};
</script>

<style scoped>
/** Responsive Design starts here **/

@media (max-width: 991px){

    .header .nav{
        justify-content: space-between;
    }

    .header .nav .top{
        display: none;
    }

    .header .nav .registeration{
        display: none;
    }

    .header .header-content .header-content-links li .start{
        padding: 1rem;
        font-size: .8rem;
        display: block;
    }

    .header .header-content .header-content-links li .learn{
        padding: 1rem;
        font-size: .8rem;
        display: block;
    }

    .header .nav #mobilemenu{
        display: block;
    }

    .header .header-content{
        padding: 0 1.5rem;
    }

    .header .header-content h1{
        font-size: 2.3rem;
    }

    .header .header-content p{
        margin-bottom: 4rem;
    }

    .header .header-content .header-content-links li a{
        padding: 1.2rem 1.5rem;
        font-size: 1rem;
    }

    .description{
        padding: 4rem 2rem 8rem;
    }

    .description h2{
        font-size: 1.8rem;
        margin-bottom: 2rem;
    }

    .description .description-content{
        flex-wrap: wrap;
    }

    .description .description-content .description-content-rightcolumn {
        position: relative;
        flex-basis: 100%;
        order: 1;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .description .description-content .description-content-rightcolumn .desktop-editor{
        display: none;
    }

    .description .description-content .description-content-rightcolumn .mobile-editor{
        display: block;
        width: 110%;
        margin-bottom: 1.5rem;
    }

    .description .description-content .description-content-leftcolumn {
        flex-basis: 100%;
        order: 2;
        text-align: center;
        margin-bottom: 3rem;
    }

    .description .description-content .description-content-leftcolumn h3{
        margin-bottom: 1rem;
    }

    .description .description-content .description-content-leftcolumn p{
        font-size: 1.1rem;
        margin-bottom: 3rem;
    }

    .services{
        padding: 8rem 2rem;
        flex-wrap: wrap;
        justify-content: space-between;
    }

    .services .services-rightcolumn{
        flex-basis: 100%;
        text-align: center;
        margin-top: 6rem;
    }

    .services .services-leftcolumn .phone{
        position: absolute;
        left: 125%;
        transform: translateX(-50%);
        top: -19rem;
        z-index: 3;
        width: 375px;
    }

    .features{
        padding: 4rem 2rem;
        flex-wrap: wrap;
    }

    .features .features-leftcolumn{
        flex-basis: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .features .features-leftcolumn .desktop-illustration{
        display: none;
    }

    .features .features-leftcolumn .mobile-illustration{
        display: block;
        width: 130%;
        margin-bottom: 1.5rem;
    }

    .features .features-rightcolumn{
        flex-basis: 100%;
        text-align: center;
    }

    .features .features-rightcolumn h5{
        font-size: 1.7rem;
    }

    footer{
        padding: 4rem 0 6rem;
        flex-wrap: wrap;
    }

    footer .down{
        flex-basis: 100%;
        text-align: center;
        margin-bottom: 3rem;
    }

    footer .attribution{
        font-size: .9rem;
    }

    footer .attribution a{
        font-size: .9rem;
    }

    #mobilenav{
        display: block;
        position: absolute;
        top: 8.5rem;
        left: 50%;
        transform: translateX(-50%);
        width: 85%;
        padding: 2rem 1.5rem;
        background: hsl(0, 0%, 100%);
        box-shadow: 0 0 30px 3px rgba(0, 0, 0, 0.3);
        text-align: center;
        border: none;
        border-radius: .5rem;
        z-index: 10;
        transition: .5s;
    }

    .mobilenav ul li{
        list-style: none;
        margin-bottom: 2rem;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .mobilenav ul li a{
        text-decoration: none;
        color: hsl(240, 10%, 16%);
        font-size: 1.2rem;
        font-weight: 300;
        font-family: 'Ubuntu', sans-serif;
        font-weight: 400;
    }

    .mobilenav ul li img{
        margin-left: .5rem;
        transition: .5s;
    }

    .mobilenav ul li:nth-child(3){
        position: relative;
    }

    .mobilenav ul li:hover img{
        transform: rotate(-180deg);
    }

    .mobilenav ul .connect{
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .mobilenav ul .connect .connect-text{
        display: flex;
        align-items: center;
    }

    .mobilenav ul .connect .drop-mobile{
        background: hsl(0, 10%, 92%);
        padding: 1.5rem 0;
        width: 100%;
        border-radius: .5rem;
        display: none;
        transition: 2s;
    }

    .mobilenav ul .connect:hover .drop-mobile{
        display: block;
    }

    .mobilenav ul .connect .drop-mobile li:last-child{
        margin-bottom: 0;
    }

    .mobilenav ul hr{
        display: block;
        border: none;
        border-top: 1px solid hsl(0, 4%, 85%);
        margin: 2rem auto 2rem;
        width: 100%;
    }

    .mobilenav ul .signup{
        margin-bottom: 0;
    }

    .mobilenav ul .signup a{
        padding: .8rem 2.5rem;
        background: linear-gradient(90deg, hsl(13, 100%, 72%), hsl(353, 100%, 62%));
        color: hsl(0, 0%, 100%);
        border-radius: 2rem;
        transition: .5s;
        font-family: 'Ubuntu', sans-serif;
        font-weight: 400;
    }

    .mobilenav ul .signup a:hover{
        background: linear-gradient(90deg, hsl(353, 100%, 62%), hsl(13, 100%, 72%));
    }
}

@media (max-width: 320px){
    .header .header-content h1{
        font-size: 1.9rem;
    }

    .header .header-content .header-content-links li .start{
        padding: 1rem;
        font-size: .8rem;
    }

    .header .header-content .header-content-links li .learn{
        padding: 1rem;
        font-size: .8rem;
    }

    .description h2{
        font-size: 1.5rem;
    }

    .description .description-content .description-content-leftcolumn h3{
        font-size: 1.5rem;
    }

    .services .services-leftcolumn .phone{
        width: 320px;
    }

    .services .services-rightcolumn{
        margin-top: 2rem;
    }

    .services .services-rightcolumn h4{
        font-size: 2.1rem;
    }

    footer .attribution{
        font-size: .7rem;
    }

    footer .attribution a{
        font-size: .7rem;
    }
}
</style>
