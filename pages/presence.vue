<template>
  <section style="height:100vh">
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css">
    <div class="column breadcumb">
      <nav class="breadcrumb is-medium" aria-label="breadcrumbs">
        <ul>
          <li><a href="#">Home</a></li>
          <li class="is-active"><a href="#" aria-current="page">Presence</a></li>
        </ul>
      </nav>
      <hr>
    </div>
    <main class="column main is-mobile">
      <div class="columns is-mobile ">
        <div class="column is-3 ">
          <p>Find Name</p>
          <br>
          <div class="field is-grouped">
            <p class="control is-expanded">
              <input class="input" type="text" placeholder="Find By Name">
            </p>
          </div>
        </div>
        <div class="column is-3">
          <p>Start Date</p>
          <br>
          <div class="field is-grouped">
            <p class="control is-expanded">
              <input class="input" type="Date" placeholder="Start Date">
            </p>
          </div>
        </div>
        <div class="column is-3">
          <p>End Date</p>
          <br>
          <div class="field is-grouped">
            <p class="control is-expanded">
              <input class="input" type="Date" placeholder="Find By Name">
            </p>
          </div>
        </div>
        <div class="column is-3">
          <br>
          <br>
          <div class="field is-grouped">
            <p class="control">
              <a class="button is-info">
                Filter
              </a>
            </p>
          </div>
        </div>
      </div>
      <div class="column is-4" style="margin-top: -50px;">
        <div class="card">
          <div class="card-content">              
              <article class="media">
                <figure class="media-left">
                  <p class="image is-64x64">
                   <img src="../assets/profile1.png">
                  </p>
                </figure>
                <div class="media-content">
                  <div class="content">
                    <p>
                      <strong>John Smith</strong>
                      <br>
                      <strong>Head of ICT Section</strong>
                    </p>
                  </div>
                  
                </div>
              </article>
          </div>
        </div>
      </div>

      <div class="columns is-multiline">

        <div class="column" style="margin-top:-50px">
          <div class="table__wrapper">
            <table class="table is-bordered pricing__table is-fullwidth">
              <thead>
                <th>
                  <center><abbr title="Position">No</abbr></center>
                </th>
                <th>
                  <center><abbr title="Played">Date</abbr></center>
                </th>
                <th>
                  <center><abbr title="Won">CheckIn Time</abbr></center>
                </th>
                <th>
                  <center><abbr title="Goal difference">CheckOut Time </abbr></center>
                </th>
                <th>
                  <center><abbr title="Goal difference">Location</abbr></center>
                </th>
                <th>
                  Status
                </th>
                <th>
                  <center><abbr title="Goal difference">Emoticon</abbr></center>
                </th>
              </thead>
              <tbody>
                <tr v-for="(data_komunitas, key) in data" :key="key">
                  <td class="center">1</td>
                  <td class="center">{{data_komunitas.date}}</td>
                  <td class="center">{{data_komunitas.checkin}}</td>
                  <td class="center">{{data_komunitas.checkout}}</td>
                  <td class="center">{{data_komunitas.location}}</td>
                  <td class="center">{{data_komunitas.status}}</td>
                  <td class="center">{{data_komunitas.emoticon}}</td>
                </tr>
              </tbody>
            </table>
          </div>
          <br>
          <nav class="pagination is-centered" role="navigation" aria-label="pagination">
            <a class="pagination-previous">Previous</a>
            <a class="pagination-next">Next page</a>
            <ul class="pagination-list">
              <li><a class="pagination-link" aria-label="Goto page 1">1</a></li>
              <li><span class="pagination-ellipsis">&hellip;</span></li>
              <li><a class="pagination-link" aria-label="Goto page 45">45</a></li>
              <li><a class="pagination-link is-current" aria-label="Page 46" aria-current="page">46</a></li>
              <li><a class="pagination-link" aria-label="Goto page 47">47</a></li>
              <li><span class="pagination-ellipsis">&hellip;</span></li>
              <li><a class="pagination-link" aria-label="Goto page 86">86</a></li>
            </ul>
          </nav>
        </div>
      </div>



    </main>

  </section>
</template>

<script>
  import Logo from '~/components/Logo.vue'

  export default {
    components: {
      Logo
    },
    data() {
      return {
        isActiveForm: false,
        data: [{
            date: '20/03/2019',
            checkin: '09:00',
            checkout: '17.30',
            location: 'TLT- Graha Merah Putih',
            status: 'Reguler',
            emoticon: 'Under Pressure',
            isActiveDrop: false,
          }, {
            date: '20/03/2019',
            checkin: '09:00',
            checkout: '17.30',
            location: 'TLT- Graha Merah Putih',
            status: 'Reguler',
            emoticon: 'Under Pressure',
            isActiveDrop: false,
          },
          {
            date: '21/03/2019',
            checkin: '09:00',
            checkout: '17.30',
            location: 'TLT- Graha Merah Putih',
            status: 'Reguler',
            emoticon: 'Comfort',
            isActiveDrop: false,
          },
          {
            date: '22/03/2019',
            checkin: '09:00',
            checkout: '17.30',
            location: 'TLT- Graha Merah Putih',
            status: 'Reguler',
            emoticon: 'Happy',
            isActiveDrop: false,
          },
        ]
      }
    },
    methods: {
      openmodal() {
        this.isActiveForm = true;

      },
      closemodal() {
        this.isActiveForm = false;
      },
      openDrop(key) {
        if (this.data[key].isActiveDrop == true) {
          this.data[key].isActiveDrop = false;
        } else {
          this.data[key].isActiveDrop = true;
        }

      }
    }
  }

</script>

<style>
  .breadcumb {
    display: block;
    flex-basis: 0;
    flex-grow: 1;
    flex-shrink: 1;
    padding: 0rem 1rem;
  }

  .hr {
    background-color: #e0dddd;
    border: none;
    display: block;
    height: 2px;
    margin: 1.5rem 0;
  }

  .main.column.main {
    padding: 0rem;
    /* margin-right: 30px; */
  }

  .center {
    text-align: center;
    
  }

  .table__wrapper {
    overflow-x: auto;
  }

  .field-body {
    display: flex;
    flex-basis: 0;
    flex-grow: 2.5;
    flex-shrink: 1;
  }

</style>
