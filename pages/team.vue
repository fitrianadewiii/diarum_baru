<template>
  <section style="height:100vh">
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css">
    <div class="column breadcumb">
      <nav class="breadcrumb is-medium" aria-label="breadcrumbs">
        <ul>
          <li><a href="#">Home</a></li>
          <li class="is-active"><a href="#" aria-current="page">My Team</a></li>
        </ul>
      </nav>
      <hr>
    </div>
    <main class="column main">
      <div class="column">
        <div class="level">
          <div class="level-left">
            <div class="level-item">
              <div class="field is-grouped">
                <p class="control is-expanded">
                  <input class="input" type="text" placeholder="Find By Name">
                </p>
                <p class="control">
                  <a class="button is-info">
                    Search
                  </a>
                </p>
              </div>
            </div>
          </div>
          <div class="level-right">
            <div class="level-item">
              <button class="button is-danger" @click="openmodal()">+ Add User</button>
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
                  <center><abbr title="Played">Nama</abbr></center>
                </th>
                <th>
                  <center><abbr title="Won">Nik</abbr></center>
                </th>
                <th>
                  <center><abbr title="Goal difference">Detail</abbr></center>
                </th>
              </thead>
              <tbody>
                <tr v-for="(data_karyawan, key) in data" :key="key">
                  <td class="center">1</td>
                  <td class="center">{{data_karyawan.nama}}</td>
                  <td class="center">secret_1234</td>

                  <td class="center">
                    <div class="dropdown is-right" @click="openDrop(key)"
                      v-bind:class="{ 'is-active': data_karyawan.isActiveDrop }">
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
            <p class="modal-card-title">Add User</p>

          </header>
          <section class="modal-card-body">
            <div class="content">
              <div class="field is-horizontal">
                <div class="field-label is-normal" style="text-align:left">
                  <label class="label">Nama</label>
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
                  <label class="label">Nik</label>
                </div>
                <div class="field-body">
                  <div class="field">
                    <p class="control">
                      <input class="input" type="text" placeholder="Nik">
                    </p>
                  </div>
                </div>
              </div>            

            </div>
          </section>
          <footer class="modal-card-foot" style="text-align:center">
            <button class="button is-success" @click="closemodal">Save changes</button>
          </footer>
        </div>
        <button class="modal-close is-large" aria-label="close" ></button>
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
          nama: 'ana',
          nik: '123',
          isActiveDrop: false
        }, {
          nama: 'asd',
          nik: '222',
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

<style scoped>
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
