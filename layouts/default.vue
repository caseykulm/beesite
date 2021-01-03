<template>
  <div>
    <nav
      class="navbar header has-shadow is-primary"
      role="navigation"
      aria-label="main navigation"
    >
      <div class="navbar-brand">
        <a
          class="navbar-item"
          href="/"
        >
          <img
            src="~assets/bee.png"
            alt="Bee Icon"
            height="28"
          >
          &nbsp;<strong>Casey's Spelling Bee Solver</strong>
        </a> 
      </div>
    </nav>

    <section class="main-content columns">
      <div class="container column is-10">
        <nuxt />
      </div>
    </section>

    <footer class="footer">
      <div class="content has-text-centered">
        <div>
          <p> Icons made by <a href="https://www.flaticon.com/authors/freepik" title="Freepik">Freepik</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a> </p>
          <p> Solver made by <a href="http://caseykulm.com">Casey Kulm</a></p>
        </div>
      </div>      
    </footer>
  </div>
</template>

<script>
export default {
  data () {
    return {
      items: [
        {
          title: 'Home',
          icon: 'home',
          to: { name: 'index' }
        }
      ]
    }
  }
}
</script>
