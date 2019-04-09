<template>
  <div>
    <navbar style="width:100%" />
    <div class="columns">

      <div class="column is-paddingless is-2" style=" background-color:  #2E363F;  margin: 10px; color:#FFF;">
        <Sidebar  />
      </div>
      <div class="column">
        <nuxt />
      </div>
    </div>
  </div>
</template>

<script>
  // import bulmaCalendar from '/node_modules/bulma-extensions/bulma-calendar/dist/bulma-calendar.min.js';
  import navbar from '../components/navbar';
  import Sidebar from '../components/Sidebar'
  // import { SidebarMenu } from 'vue-sidebar-menu'
  export default {
    components: {
      navbar,
      Sidebar
      // SidebarMenu
    },
    data:()=>({
    active:false,
  }),
  methods: {
    onCollapse(collapsed) {},
    onItemClick(event, item) {}
}
  }
   

</script>


<style>
  .menu-list a {
    border-radius: 2px;
    color: #ffffff;
    display: block;
    padding: 0.5em 0.75em;
  }

  .menu-label {
    color: #ffffff;
    font-size: 0.75em;
    letter-spacing: 0.1em;
    text-transform: uppercase;
  }

</style>
