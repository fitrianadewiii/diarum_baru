<template>
  <section>

    <header>
      <div id="app">
        <nav class="navbar" role="navigation" aria-label="main navigation">
          <div class="navbar-brand">
            <a class="navbar-item">
              <img src="https://bulma.io/images/bulma-logo.png" width="112" height="28">
            </a>

            <a role="button" style="color:#FFF" class="navbar-burger" @click="active=!active"
              >
              <span aria-hidden="true"></span>
              <span aria-hidden="true"></span>
              <span aria-hidden="true"></span>
            </a>
          </div>

          <div id="" class="navbar-menu">
            <div class="navbar-start">


            </div>

            <div class="navbar-end">
              <div class="navbar-item">

              </div>
            </div>
          </div>
        </nav>
      </div>
    </header>
  </section>
</template>
<script>

</script>
<style>
  aside.column.is-2 {
    background-color: #2E363F;
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
    background-color: #2E363F;
  }

  .navbar-item,
  .navbar-link {
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
