<template>
  <section style="height:100vh">
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css">
    <div class="column breadcumb">
      <nav class="breadcrumb is-medium" aria-label="breadcrumbs">
        <ul>
          <li><a href="#">Home</a></li>
          <li class="is-active"><a href="#" aria-current="page">Community</a></li>
        </ul>
      </nav>
      <hr>
    </div>
    <main class="column main">
      <div class="column">
        <div class="level">
          <div class="level-left">

          </div>
          <div class="level-right">
            <div class="level-item">
              <button class="button is-danger" @click="openmodal()">+ Add Community</button>
            </div>
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
                  <center><abbr title="Played">Foto</abbr></center>
                </th>
                <th>
                  <center><abbr title="Won">Nama Komunitas</abbr></center>
                </th>
                <th>
                  <center><abbr title="Goal difference">Jenis</abbr></center>
                </th>
                <th>
                  <center><abbr title="Goal difference">Jumlah Member</abbr></center>
                </th>
                <th>
                  <center><abbr title="Goal difference">Aksi</abbr></center>
                </th>
              </thead>
              <tbody>
                <tr v-for="(data_komunitas, key) in data" :key="key">
                  <td class="center">1</td>
                  <td class="center">
                    <center>
                      <figure class="image is-64x64">
                        <img src="../assets/image.jpg">
                      </figure>
                    </center>
                  </td>
                  <td class="center">{{data_komunitas.nama}}</td>
                  <td class="center">{{data_komunitas.jenis}}</td>
                  <td class="center">{{data_komunitas.jumlahmember}}</td>
                  <td class="center">
                    <div class="dropdown is-right" @click="openDrop(key)"
                      v-bind:class="{ 'is-active': data_komunitas.isActiveDrop }">
                      <div class="dropdown-trigger">
                        <button class="button is-success" aria-haspopup="true" aria-controls="dropdown-menu6">
                          <span>Action</span>
                          <span class="icon is-small">
                            <i class="fa fa-angle-down" aria-hidden="true"></i>
                          </span>
                        </button>
                      </div>
                      <div class="dropdown-menu" id="dropdown-menu6" role="menu">
                        <div class="dropdown-content">
                          <a class="dropdown-item" href="detail_team.vue">
                            Details
                          </a>
                          <a class="dropdown-item">
                            Edit
                          </a>
                          <a href="#" class="dropdown-item is-active">
                            Delete
                          </a>
                        </div>
                      </div>
                    </div>
                  </td>

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

      <div class="modal" v-bind:class="{ 'is-active': isActiveForm }">
        <div class="modal-background"></div>
        <div class="modal-card">
          <header class="modal-card-head">
            <p class="modal-card-title">Add Community</p>

          </header>
          <section class="modal-card-body">
            <div class="content">
              <div class="field is-horizontal">
                <div class="field-label is-normal" style="text-align:left">
                  <label class="label">Nama Community</label>
                </div>
                <div class="field-body">
                  <div class="field">
                    <p class="control">
                      <input class="input" type="text" placeholder="Nama">
                    </p>
                  </div>
                </div>
              </div>
              <div class="field is-horizontal">
                <div class="field-label is-normal" style="text-align:left">
                  <label class="label">Jenis Community</label>
                </div>
                <div class="field-body">
                  <div class="field">
                   <div class="select">
                        <select>
                          <option>Public</option>
                          <option>Private</option>
                        </select>
                      </div>
                  </div>
                </div>
              </div>
              <div class="field is-horizontal">
                <div class="field-label is-normal" style="text-align:left">
                  <label class="label">Jumlah Member</label>
                </div>
                <div class="field-body">
                  <div class="field">
                    <div class="control">
                      <div class="select">
                        <select>
                          <option>1</option>
                          <option>2</option>
                          <option>3</option>
                          <option>4</option>
                          <option>5</option>
                          <option>6</option>
                        </select>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
              <div class="field is-horizontal">
                <div class="field-label is-normal" style="text-align:left">
                  <label class="label">Choose Member</label>
                </div>
              </div>
              <div class="field is-horizontal">
                <table class="table is-bordered pricing__table is-fullwidth">   
                  <thead>
                    
                    <th>
                      <center><abbr title="Won">Nama Member</abbr></center>
                    </th>
                  </thead>
                  <tbody>
                    <tr>                    
                      <td class="">
                        <label class="checkbox">
                          <input type="checkbox">
                          Nama satu
                        </label>
                      </td>
                    </tr>
                    <tr>                    
                      <td class="">
                        <label class="checkbox">
                          <input type="checkbox">
                          Nama satu
                        </label>
                      </td>
                    </tr>
                    <tr>                    
                      <td class="">
                        <label class="checkbox">
                          <input type="checkbox">
                          Nama satu
                        </label>
                      </td>
                    </tr>
                    <tr>                    
                      <td class="">
                        <label class="checkbox">
                          <input type="checkbox">
                          Nama satu
                        </label>
                      </td>
                    </tr>
                    <tr>                    
                      <td class="">
                        <label class="checkbox">
                          <input type="checkbox">
                          Nama satu
                        </label>
                      </td>
                    </tr>
                  </tbody>
                </table>
              </div>
              

            </div>
          </section>
          <footer class="modal-card-foot" style="text-align:center">
            <button class="button is-success" @click="closemodal">Save changes</button>
         
          </footer>
        </div>
        <button class="modal-close is-large" aria-label="close"></button>
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
          nama: 'komunitas frontend developer',
          jenis: 'public',
          jumlahmember: '20',
          isActiveDrop: false
        }, {
          nama: 'komunitas back end developer',
          jenis: 'private',
          jumlahmember: '20',
          isActiveDrop: false
        }]
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

<style >
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
