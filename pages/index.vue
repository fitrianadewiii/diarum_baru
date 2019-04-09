<template>
   <section class="login is-fullheight background-login">
      <div class="login-body" >
        <div class="container v-middle ">
          <div class="columns  login-page " >
              <div class="column is-5 login-sidebar ">
                <div class="login-gradient-background">
                </div>
              </div>
              <div class="column is-7 login-form-side2">
                <div class="column is-12 has-text-right register-btn">
                  <!-- <a class="btn" name="button">Register</a> -->
                </div>
                <div class="column is-12 field-box">
                  <div class="column is-7 is-offset-1">
                    <h1 class="login-heading" >Welcome to Diarium</h1> 
                    <br>
                    <br>                  
                    <form method="" action="">
                      <div class="field">
                        <p class="control has-icons-left has-icons-right">
                          <input class="input is-normal" type="email" placeholder="Email" value="" name="email" autofocus="" required>
                          <span class="icon is-normal is-left">
                            <i class="fa fa-envelope"></i>
                          </span>
                          <span class="icon is-small is-right">
                            <i class="fa fa-check"></i>
                          </span>
                        </p>
                      </div>
                      <div class="field">
                        <p class="control has-icons-left has-icons-right">
                          <input class="input is-normal" type="password" placeholder="Password" name="password" required>
                          <span class="icon is-normal is-left">
                            <i class="fa fa-lock"></i>
                          </span>
                          <span class="icon is-small is-right">
                            <i class="fa fa-eye"></i>
                          </span>
                        </p>
                      </div>
                      <div class="field is-grouped is-grouped-left login-btn-group">
                        <p class="control">
                          <a class="login-btn">
                            Login
                          </a>
                        </p>
                        <p class="control">
                          <a class="forgot-link" >Forgot Password</a>
                        </p>
                      </div>
                    </form>
                  </div>
                </div>
              </div>
          </div>
        </div>
      </div>
  </section>
</template>

<script>
import Logo from '~/components/Logo.vue'
import loginVue from '../layouts/login.vue';

export default {
  layout : 'login',
  components: {
    Logo
  },

}
</script>

<style>


  .boxshadows{   
    border-radius: 5px;    
    border-left-color: #E7EAED;
    border-top-color: #E7EAED;
  }
  .background-login{
    background: url('../assets/gambar.jpg');
    background-size: cover;
  }
  .login{
    min-height: 100vh;
    background-color: #f7f7f7;
    
  }
  .login .login-page{
    height: 100vh;display: flex;align-items: center;
  }
  .login .login-sidebar{
    background: #fff;height: 80vh;
    border-bottom-left-radius: 5px;
    border-top-left-radius: 5px;
     padding: 10px;
     box-shadow: 0px 3px 0px 0px #E7EAED;
  }
   .login-form-side2{
    background: #fff;height: 80vh;
    border-bottom-right-radius: 5px;
    border-top-right-radius: 5px;
    padding: 10px;
    border: #E7EAED solid 2px;
    box-shadow: 3px 3px 0px 0px #E7EAED;
  }
  .login .login-sidebar{
    background:  url('../assets/square2.jpg')center center no-repeat;
    background-size: cover;
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
  }
  .login .login-sidebar::before{
    content: '';
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    z-index: 1;
    opacity: .8;
  }
  .login .login-sidebar .login-gradient-background{
    position: absolute;z-index: 2;
  }
  .login .login-sidebar .login-gradient-background h1{
    font-size: 2em;font-weight: 600;text-transform: uppercase;color: #ffffff;
  }

  .login-form-side2.register-btn a{
    color: #ffffff;border-radius: 18px;padding: 0.57em 2em;background: #CE1000;
  }
  .login-form-side2 .register-btn a:hover{
    opacity: .8;
  }
  .field-box .field{
    margin-bottom: 1.5em;
    }
  .login-form-side2 .field-box{
    display: flex;
    height: 80%;
    align-items: center;
  }
  .login-form-side2 .field-box .login-heading{
    font-size: 1.95em;
    color: #CE1000;
  }
  .login-form-side2 .field-box .login-subheading{
    margin-bottom: 2em;
    font-size: 0.85em;
    color: #787877;
  }

  .login-form-side2 .field-box .login-btn-group .login-btn{
    background: #DB5146;
    color: #ffffff;
    border-radius: 10px;
    padding: 0.57em 2em;
  }
  .login-form-side2 .field-box .login-btn-group .forgot-link{
    color: #777777;
    font-size: 0.85em;
  }
  .login-form-side2 .field-box .login-btn-group .forgot-link:hover{
    color: #444444;
    font-size: 0.85em;
  }


</style>
