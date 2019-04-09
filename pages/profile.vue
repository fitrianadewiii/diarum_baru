<template>
   <section>
    <div class="container is-widescreen">
        
        <div class="column nav-container">
                <!-- navbar -->
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
                    <a class="navbar-item">
                        Home
                    </a>

                    <a class="navbar-item">
                        Documentation
                    </a>

                    <div class="navbar-item has-dropdown is-hoverable">
                        <a class="navbar-link">
                        More
                        </a>

                        <div class="navbar-dropdown">
                        <a class="navbar-item">
                            About
                        </a>
                        <a class="navbar-item">
                            Jobs
                        </a>
                        <a class="navbar-item">
                            Contact
                        </a>
                        <hr class="navbar-divider">
                        <a class="navbar-item">
                            Report an issue
                        </a>
                        </div>
                    </div>
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
        </div>
        <div class="column">
                <!-- background top -->
            <section class="hero is-primary is-bold">
                <div class="hero-body">
                    <div class="container">
                    <h1 class="title">
                        <figure class="media-left" >
                        <p class="image is-128x128">
                            <img class="is-rounded" src="../assets/profile.png" >
                        </p>
                    </figure>
                    </h1>
                    <h2 class="subtitle">
                        John Doe | Head Of ICT
                    </h2>
                    </div>
                </div>
            </section>
            <!-- image and information -->
            <div class="columns is-mobile">
                <div class="column">
                    <div class="tabs is-centered">
                        <ul>
                            <li class="is-active">
                            <a>
                                <center>
                                <span>
                                    <b>10</b>
                                    <br>
                                    Post                          
                                </span>
                                </center>
                            </a>
                            </li>
                            <li>
                            <a>
                                <center>
                                <span>
                                    <b>10</b>
                                    <br>
                                    Friends                           
                                </span>
                                </center>
                            </a>
                            </li>
                            <li>
                            <a>
                                <center>
                                <span>
                                    <b>10</b>
                                    <br>
                                    Followers                           
                                </span>
                                </center>
                            </a>
                            </li>
                            <li>
                            <a>
                                <center>
                                <span>
                                    <b>10</b>
                                    <br>
                                    Community                           
                                </span>
                                </center>
                            </a>
                            </li>                       
                        </ul>
                    </div>
                </div>
            </div>
        </div>
        <!-- BODY PROFILE -->
        <div class="columns" style="background-color: #E6ECF0; padding:10px">
            <div class="column is-3">
               <div class="card">
                    
                    <div class="card-content">
                        <div class="media">
                        <div class="media-left">
                            <figure class="image is-48x48">
                            <img src="../assets/profile.png" alt="Placeholder image">
                            </figure>
                        </div>
                        <div class="media-content">
                            <p class="title is-4">John Doe</p>
                            <p class="subtitle is-6">Head Of ICT Solution</p>
                        </div>
                        </div>

                        <div class="content">
                        " A dream doesn't become reality through magic; it takes sweat, determination and hard work." 
                        <br>
                        <br>
                        <b>NIK : 12345 | Bandung</b>
                        <br>
                        
                        </div>
                    </div>
                </div>             
            </div>
            <div class="column is-6">
                <div class="column is-12 ">
                    <article class="media">
                        <figure class="media-left">
                            <p class="image is-64x64">
                            <img class="is-rounded" src="../assets/profile.png">
                            </p>
                        </figure>
                        <div class="media-content">
                            <div class="field">
                            <p class="control">
                                <textarea class="textarea" placeholder="Add a comment..."></textarea>
                            </p>
                            </div>
                            <div class="columns is-mobile">
                                <div class="column">
                                    <a class="button is-info">Submit</a>
                                </div>
                                    <div class="column">
                                    <label class="checkbox">
                                        <input type="checkbox"> Press enter to submit
                                    </label>
                                </div>
                            </div>
                        </div>
                    </article>
                </div>
                <br>
                <div class="card">                    
                    <div class="card-content">

                        <article class="media">
                            <figure class="media-left">
                                <p class="image is-64x64">
                                 <img class="is-rounded" src="../assets/profile.png">
                                </p>
                            </figure>
                            <div class="media-content">
                                <div class="content">
                                <p>
                                    <strong>John Smith</strong> <small>@johnsmith</small> <small>31m</small>
                                    <br>
                                    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin ornare magna eros, eu pellentesque tortor vestibulum ut. Maecenas non massa sem. Etiam finibus odio quis feugiat facilisis.
                                </p>
                                </div>
                                <nav class="level is-mobile">
                                <div class="level-left">
                                    <a class="level-item">
                                    <span class="icon is-small"><i class="fas fa-reply"></i></span>
                                    </a>
                                    <a class="level-item">
                                    <span class="icon is-small"><i class="fas fa-retweet"></i></span>
                                    </a>
                                    <a class="level-item">
                                    <span class="icon is-small"><i class="fas fa-heart"></i></span>
                                    </a>
                                </div>
                                </nav>
                            </div>
                            <!-- <div class="media-right">
                                <button class="delete"></button>
                            </div> -->
                        </article>

                        <article class="media">
                            <figure class="media-left">
                                <p class="image is-64x64">
                                <img class="is-rounded" src="../assets/profile.png">
                                </p>
                            </figure>
                            <div class="media-content">
                                <div class="content">
                                <p>
                                    <strong>Barbara Middleton</strong>
                                    <br>
                                    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis porta eros lacus, nec ultricies elit blandit non. Suspendisse pellentesque mauris sit amet dolor blandit rutrum. Nunc in tempus turpis.
                                    <br>
                                    <small><a>Like</a> · <a>Reply</a> · 3 hrs</small>
                                </p>
                                </div>

                                <article class="media">
                                <figure class="media-left">
                                    <p class="image is-48x48">
                                    <img class="is-rounded" src="../assets/profile1.png">
                                    </p>
                                </figure>
                                <div class="media-content">
                                    <div class="content">
                                    <p>
                                        <strong>Sean Brown</strong>
                                        <br>
                                        Donec sollicitudin urna eget eros malesuada sagittis. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Aliquam blandit nisl a nulla sagittis, a lobortis leo feugiat.
                                        <br>
                                        <small><a>Like</a> · <a>Reply</a> · 2 hrs</small>
                                    </p>
                                    </div>

                                    <article class="media">
                                    Vivamus quis semper metus, non tincidunt dolor. Vivamus in mi eu lorem cursus ullamcorper sit amet nec massa.
                                    </article>

                                    <article class="media">
                                    Morbi vitae diam et purus tincidunt porttitor vel vitae augue. Praesent malesuada metus sed pharetra euismod. Cras tellus odio, tincidunt iaculis diam non, porta aliquet tortor.
                                    </article>
                                </div>
                                </article>

                                <article class="media">
                                <figure class="media-left">
                                    <p class="image is-48x48">
                                    <img class="is-rounded" src="../assets/profile2.png">
                                    </p>
                                </figure>
                                <div class="media-content">
                                    <div class="content">
                                    <p>
                                        <strong>Kayli Eunice </strong>
                                        <br>
                                        Sed convallis scelerisque mauris, non pulvinar nunc mattis vel. Maecenas varius felis sit amet magna vestibulum euismod malesuada cursus libero. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Phasellus lacinia non nisl id feugiat.
                                        <br>
                                        <small><a>Like</a> · <a>Reply</a> · 2 hrs</small>
                                    </p>
                                    </div>
                                </div>
                                </article>
                            </div>
                            </article>
                            <article class="media">
                            <figure class="media-left">
                                <p class="image is-64x64">
                                 <img class="is-rounded" src="../assets/profile.png">
                                </p>
                            </figure>
                            <div class="media-content">
                                <div class="field">
                                <p class="control">
                                    <textarea class="textarea" placeholder="Add a comment..."></textarea>
                                </p>
                                </div>
                                <div class="field">
                                <p class="control">
                                    <button class="button">Post comment</button>
                                </p>
                                </div>
                            </div>
                        </article>
                        
                    </div>
                    <footer class="card-footer">
                      
                    </footer>
                </div>            
            </div>
            <div class="column is-3">   
                <div class="card">
                    <header class="card-header">
                        <p class="card-header-title">
                        Who to Follow
                        </p>                   
                    </header>
                    <div class="card-content content-for-friends">
                       
                        <div class="columns col-for-friends is-mobile">
                            <figure class="media-left">
                                <p class="image img-center is-64x64">
                                 <img class="is-rounded" src="../assets/profile1.png">
                                </p>
                            </figure>
                            <div class="column is-mobile ">
                                <div class="columns">
                                    <p><b>Marion Jolla</b></p>
                                </div>
                                <div class="columns">
                                    <p>1234567</p>
                                </div>
                                <div class="columns is-mobile" style="margin-top:-20px" >
                                    <div class="column ">
                                         <a class="button is-danger is-small is-fullwidth is-rounded btnred">Confirm sad</a>   
                                    </div>
                                     <div class="column ">
                                         <a class="button is-danger  is-outlined is-small  is-fullwidth is-rounded">Reject</a>  
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="columns col-for-friends is-mobile">
                            <figure class="media-left">
                                <p class="image img-center is-64x64">
                                 <img class="is-rounded" src="../assets/profile2.png">
                                </p>
                            </figure>
                            <div class="column is-mobile ">
                                <div class="columns">
                                    <p><b>Marion Jolla</b></p>
                                </div>
                                <div class="columns">
                                    <p>1234567</p>
                                </div>
                                <div class="columns is-mobile" style="margin-top:-20px" >
                                    <div class="column ">
                                         <a class="button is-danger is-small is-fullwidth is-rounded btnred">Confirm</a>   
                                    </div>
                                     <div class="column ">
                                         <a class="button is-danger  is-outlined is-small  is-fullwidth is-rounded">Reject</a>  
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="columns col-for-friends is-mobile">
                            <figure class="media-left">
                                <p class="image img-center is-64x64">
                                 <img class="is-rounded" src="../assets/profile1.png">
                                </p>
                            </figure>
                            <div class="column is-mobile ">
                                <div class="columns">
                                    <p><b>Marion Jolla</b></p>
                                </div>
                                <div class="columns">
                                    <p>1234567</p>
                                </div>
                                <div class="columns is-mobile" style="margin-top:-20px" >
                                    <div class="column ">
                                         <a class="button is-danger is-small is-fullwidth is-rounded btnred">Confirm</a>   
                                    </div>
                                     <div class="column ">
                                         <a class="button is-danger  is-outlined is-small  is-fullwidth is-rounded">Reject</a>  
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="columns col-for-friends is-mobile">
                            <figure class="media-left">
                                <p class="image img-center is-64x64">
                                 <img class="is-rounded" src="../assets/profile2.png">
                                </p>
                            </figure>
                            <div class="column is-mobile ">
                                <div class="columns">
                                    <p><b>Marion Jolla</b></p>
                                </div>
                                <div class="columns">
                                    <p>1234567</p>
                                </div>
                                <div class="columns is-mobile" style="margin-top:-20px" >
                                    <div class="column ">
                                         <a class="button is-danger is-small is-fullwidth is-rounded btnred">Confirm</a>   
                                    </div>
                                     <div class="column ">
                                         <a class="button is-danger  is-outlined is-small  is-fullwidth is-rounded">Reject</a>  
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="columns col-for-friends is-mobile">
                            <figure class="media-left">
                                <p class="image img-center is-64x64">
                                 <img class="is-rounded" src="../assets/profile1.png">
                                </p>
                            </figure>
                            <div class="column is-mobile ">
                                <div class="columns">
                                    <p><b>Marion Jolla</b></p>
                                </div>
                                <div class="columns">
                                    <p>1234567</p>
                                </div>
                                <div class="columns is-mobile" style="margin-top:-20px" >
                                    <div class="column ">
                                         <a class="button is-danger is-small is-fullwidth is-rounded btnred">Confirm</a>   
                                    </div>
                                     <div class="column ">
                                         <a class="button is-danger  is-outlined is-small  is-fullwidth is-rounded">Reject</a>  
                                    </div>
                                </div>
                            </div>
                        </div>
                        

                       
                    </div>
                    
                    <footer class="card-footer">                       
                        <p class="link">
                        <a><u> View More </u></a>
                        </p>                         
                    </footer>
                </div>  
                   
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

.nav-container {
    max-width: 100%;
    width: 100%;
    padding: 0px;
    
}
.container {
    max-width: 100%;
    width: 100%;
    padding: 0px;
    
}
.columntopbar {
    height: 250px;
    /* width: 100%; */
    background: url('../assets/dark.jpg')center center no-repeat;
    background-size: cover;
    
}

.image{
    text-align: bottom;
    height: 230px;
}

.imgcenter{
    margin-left: auto;
    margin-right: auto;
}

.image.is-128x128 {
    height: 150px;
    width: 150px;
    margin-left: 10px;
}
.image.is-128x128small {
    height: 35px;
    width: 35px;
}
.center {
  float: center;
}
.right {
  float:right;
}
.input.is-rounded {
    border-radius: 290486px;
    padding-left: 1em;
    /* padding-right: 2em; */
    /* margin-right: 20px; */
    width: 100%;
}

.link {
    
    align-items:right;
    color: blue;
    display: flex;
    flex-grow: 1;
    font-weight: 500;
    padding: 0.75rem;
}

.col-for-friends{
    border-bottom: 1px #EDEDED solid;
}

.content-for-friends{
    max-height: 300px;
    height: 90%;
    overflow: auto;
}

.btnred{
    color: #FFF;
    font-weight: bold;
    float: left
}
/* .all{
    background-color: #E6ECF0;
} */
</style>
   