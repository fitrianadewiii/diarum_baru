<template>
  <section>
    <div class="section">
      <div class="navbar-menu" v-bind:class="{ active}">
        <div class="columns">
          <aside class="column">
            <nav class="menu">
              <p class="menu-label">
                General
              </p>
              <ul class="menu-list">
                <li><a class="is-active" href="..//home.vue">Dashboard</a></li>
                <li><a>Presence</a></li>
                <li><a>Report Activity</a></li>
                <li><a>Team</a></li>
                <li><a>News</a></li>

              </ul>
              <p class="menu-label">
                Administration
              </p>
            </nav>
          </aside>


        </div>
      </div>

    </div>
  </section>
</template>
<script>
  export default {

  }

</script>
<style>

</style>
