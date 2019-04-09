<template>
    <section>
        <header >
          <nav class="navbar" role="navigation" aria-label="main navigation">
            <div class="navbar-brand">
              <a class="navbar-item" href="https://bulma.io">
                <img src="https://bulma.io/images/bulma-logo.png" width="112" height="28">
              </a>

              <a role="button" class="navbar-burger burger" aria-label="menu" aria-expanded="false" data-target="navbarBasicExample">
                <span aria-hidden="true"></span>
                <span aria-hidden="true"></span>
                <span aria-hidden="true"></span>
              </a>
            </div>

          <div id="navbarBasicExample" class="navbar-menu">
            <div class="navbar-start">
            

            </div>

            <div class="navbar-end">
              <div class="navbar-item">
                <div class="buttons">
                  <a class="button is-primary">
                    <strong>Sign up</strong>
                  </a>
                  <a class="button is-light">
                    Log in
                  </a>
                </div>
              </div>
            </div>
          </div>
        </nav>
      </header>
    </section>
</template>
<script>
    
</script>
<style>
aside.column.is-2 {
    background-color: #e0e0e0;
    padding: 3rem 1.5rem;
}
.column {
    display: block;
    flex-basis: 0;
    flex-grow: 1;
    flex-shrink: 1;
    padding: 3rem 1.5rem;
}
.navbar {
    min-height: 3.25rem;
    background-color: #ce1000;
}
.navbar-item, .navbar-link {
    color: #ffffff;
    display: block;
    line-height: 1.5;
    padding: 0.5rem 0.75rem;
    position: relative;
}
.navbar-link:not(.is-arrowless)::after {
    border-color: #ffffff;
    margin-top: -0.375em;
    right: 1.125em;
}
.section {
    padding: 0rem;
}

</style>
