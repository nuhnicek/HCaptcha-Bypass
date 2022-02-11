












<!DOCTYPE html>
<html lang="cz">

<head>
  <meta charset="utf-8">
  <meta content="width=device-width, initial-scale=0.8" name="viewport">

  <title>Administrace | 🍐 PearHost.cz</title>
  <meta content="Administrace PearHost.cz" name="desc">
  <meta content="Flukysek" name="author">

  <!-- Ikonka -->
  <link href="https://pearhost.cz/assets/img/icon.png" rel="icon">

  <!-- CSS -->
  <link href="https://pearhost.cz/assets/vendor/bootstrap/css/bootstrap.min.css" rel="stylesheet">
  <link href="https://pearhost.cz/assets/vendor/icofont/icofont.min.css" rel="stylesheet">
  <link href="https://pearhost.cz/assets/vendor/boxicons/css/boxicons.min.css" rel="stylesheet">
  <link href="https://pearhost.cz/assets/vendor/animate.css/animate.min.css" rel="stylesheet">

  <!-- FlukyCss -->
  <link href="assets/style.css?v=1644607068" rel="stylesheet">

  <!-- Ostatni -->
  
  <script src="https://pearhost.cz/8a0a48c216.js" crossorigin="anonymous"></script>
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
  <script src="https://cdn.jsdelivr.net/gh/leonardosnt/mc-player-counter/dist/mc-player-counter.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.7/umd/popper.min.js" integrity="sha384-UO2eT0CpHqdSJQ6hJty5KVphtPhzWj9WO1clHTMGa3JDZwrnQq4sF86dIHNDz0W1" crossorigin="anonymous"></script>
  <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/js/bootstrap.min.js" integrity="sha384-JjSmVgyd0p3pXB1rRibZUAYoIIy6OrQ6VrjIEaFf/nJGzIxFDsf4x0xIM+B07jRM" crossorigin="anonymous"></script>
  <script src="//cdn.jsdelivr.net/npm/sweetalert2@11/dist/sweetalert2.min.js"></script>
  <link rel="stylesheet" href="//cdn.jsdelivr.net/npm/sweetalert2@11/dist/sweetalert2.min.css">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css" integrity="sha512-1ycn6IcaQQ40/MKBW2W4Rhis/DbILU74C1vSrLJxCq57o941Ym01SwNsOMqvEBFlcgUa6xLiPY/NS5R+E6ztJQ==" crossorigin="anonymous" referrerpolicy="no-referrer" />
</head>

<style>
@import url('https://fonts.googleapis.com/css2?family=Ubuntu:wght@300&display=swap');
</style>
 




<body>

<style>

  .vpsrow{
    background-color:#32383E;width:99.34%;height:100px;margin-bottom:17.5px;border-radius: 0.25rem;position:relative;margin-left:5px;
  }
  .vpsrow:hover{
    background:#1D2328;
    border-left: 5px solid #068B1C;
  }
  .vpsicon{
    background-color:#28A745;position:absolute;padding:15px;border-radius: 100px;
    transform: translateY(-50%);
    top:50%;
    left:20px;
    position:absolute;
  }
  .vpsname {
    font-size:25px;font-family:"Ubuntu";
    line-height: 100px;
    margin-left:90px;

  } 
  .mcrow{
    background-color:#32383E;width:99.34%;height:100px;margin-bottom:17.5px;border-radius: 0.25rem;position:relative;margin-left:0px;
  }
  .mcrow:hover{
    background:#1D2328;
    border-left: 5px solid #068B1C;
  }
  .mcicon{
    background-color:#28A745;position:absolute;padding:15px;border-radius: 100px;
    transform: translateY(-50%);
    top:50%;
    left:20px;
    position:absolute;
  }
  .mcname {
    position:absolute;
    font-size:25px;font-family:"Ubuntu";
    top:50%;
    transform: translateY(-50%);
    left:90px;

  } 
  @media only screen and (max-device-width: 768px) {
    #ipspan {display:none;}
  }
  
  .switcher {
    min-width: 220px;
  }
</style>  




<nav class="navbar sticky-top navbar-light" style="background-color: #068B1C;z-index:1000;">
<a class="navbar-brand pcsidebarbrand">🍐<span style="color: #28A745;"><strong>Pear</strong></span><span style="color: #fff;">Host.cz</span></a>
<a class="navbar-brand mobilesidebarbrand">🍐</a>
    
 

<button onclick='changesidebar("mobile");' style="top:15px;height:35px;width:35px;padding:0;" id="pc_changesidebar_button" class="btn btn-success"><i style="position:absolute;top:10px;bottom:10px;left:10px;right:10px;" class="fas fa-bars"></i></button>
<button onclick='changesidebar("pc");' style="top:15px;height:35px;width:35px;padding:0;" id="mobile_changesidebar_button" class="btn btn-success"><i style="position:absolute;top:10px;bottom:10px;left:10px;right:10px;" class="fas fa-bars"></i></button>




<script>
  function changesidebar(parametr){
    if(parametr === "pc"){
      document.getElementsByClassName("sidebar")[0].style.left = "0";
      document.getElementsByClassName("wrapper")[0].style.marginLeft = "280px";
      document.getElementsByClassName("mobilesidebarbrand")[0].style.display = "none";
      document.getElementById("pc_changesidebar_button").style.display = "block";
      document.getElementById("pc_changesidebar_button").style.position = "fixed";
      document.getElementById("pc_changesidebar_button").style.left = "255px";
      document.getElementById("mobile_changesidebar_button").style.display = "none";
      document.getElementsByClassName("pcsidebarbrand")[0].style.display = "block";
      if(window.innerWidth<801){
        document.getElementById("adminbutton").style.display = "none";
      }
      
    }
    if(parametr === "mobile"){
      document.getElementsByClassName("pcsidebarbrand")[0].style.display = "none";
      document.getElementsByClassName("mobilesidebarbrand")[0].style.display = "block";
      document.getElementsByClassName("mobilesidebarbrand")[0].style.marginLeft = "40px";
      document.getElementById("mobile_changesidebar_button").style.display = "block";
      document.getElementById("mobile_changesidebar_button").style.position = "fixed";
      document.getElementById("mobile_changesidebar_button").style.left = "10px";
      document.getElementById("pc_changesidebar_button").style.display = "none";
      document.getElementsByClassName("wrapper")[0].style.marginLeft = "15px";
      document.getElementsByClassName("sidebar")[0].style.left = "-255px";
      document.getElementById("adminbutton").style.display = "block";
      
    }
  }
</script>  

<style>

    #profileDD .profilepic {
    display: block;
    z-index: 2002;
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center center;
    background-image: url("https://www.gravatar.com/avatar/bb6a46df703340020976a8dba76613f6?d=https%3A%2F%2Fupload.wikimedia.org%2Fwikipedia%2Fcommons%2F9%2F99%2FSample_User_Icon.png&s=100");
    width: 40px;
    height: 40px;
    border-radius: 50%;
    position:absolute;
    box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;

    top: 50%;transform: translateY(-50%);
  }

  #profileDD .profilename {
    font-family: sans-serif;
    font-size:120%;
    position:relative;
    color: white;
    font-weight: bold;
    margin:0;
    text-align:left;
    margin-left:50px;
    margin-right:25px;
    padding:0;
    width:fit-content;

  }
  #profileDD .arrowdown {
    font-size:110%;
    position:absolute;
    top: 25%;transform: translateY(-50%);
    right:10px;
    color: white;

    -webkit-transform: rotate(-90deg);
  }

  #profileDD .profile {
    border:none;
    outline: none;
    background: transparent;
    z-index: 2000;
    margin:0;
    padding:0;
    display:block;
    min-width: 175px;
    height:50px;
  }

  #profileDD .profile:focus{
    outline: none;
    border:none;
  }
  #profileDD .dropdown-item:hover {
    transition-duration: 0.5s;
    color: white;
    box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
    background:transparent;
  }
  #profileDD .dropdown-item:focus {
    color: white;
    box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
    background:transparent;
  }

  #profileDD .dropdown-item{
    color: white !important;
    transition-duration: 0.5s;
    cursor:pointer;
    padding: 1rem 1.5rem;
    user-select: none;
    font-size:100%;
  }
  #profileDD .dropdown-item i {
    font-size:120%;
    color:#068B1C;
  }
  #profileDD .dropdown-menu {
    width:250px;
    right:0;
    left:auto;
  }
  #profileDD .dropdown-divider{
    height:0;
    margin: 0;
    border-top: 1px solid rgba(0,0,0,.20);
  }

  @media (min-width: 768px) {
  .animateDD {
    animation-duration: 0.3s;
    -webkit-animation-duration: 0.3s;
    animation-fill-mode: both;
    -webkit-animation-fill-mode: both;
  }
}

@keyframes slideIn {
  0% {
    transform: translateY(1rem);
    opacity: 0;
  }

  100% {
    transform: translateY(0rem);
    opacity: 1;
  }

  0% {
    transform: translateY(1rem);
    opacity: 0;
  }
}

@-webkit-keyframes slideIn {
  0% {
    -webkit-transform: transform;
    -webkit-opacity: 0;
  }

  100% {
    -webkit-transform: translateY(0);
    -webkit-opacity: 1;
  }

  0% {
    -webkit-transform: translateY(1rem);
    -webkit-opacity: 0;
  }
}

.slideIn {
  -webkit-animation-name: slideIn;
  animation-name: slideIn;
}
</style>  



<div class="dropdown" id="profileDD">
  
  <button class="profile" data-toggle="dropdown">
    <div class="profilepic"></div>
    <div class="profilename">nuhnicek</div>
    <div class="arrowdown"><i class="fas fa-sort-down"></i></div>
  </button>
  <!--   <button class="btn btn-success fa-margin my-2 my-sm-0 dropdown-toggle" type="button" id="dropdownMenuButton" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
  <i class="fas fa-user-circle"></i> Zákaznický účet
  </button> -->
    <div class="dropdown-menu animateDD slideIn" style="background:#32383E;" aria-labelledby="dropdownMenuButton">
    <a style="position:relative;" class="dropdown-item"><i style="position:absolute;top: 50%;transform: translateY(-50%);" class="fas fa-wallet"></i>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;10 Kreditů</a>
    <div class="dropdown-divider"></div>
    <a style="position:relative;" class="dropdown-item" onclick="location.href='/client/profil'"><i style="position:absolute;top: 50%;transform: translateY(-50%);" class="fas fa-user-cog"></i>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Nastavení účtu</a>
    <a style="position:relative;" class="dropdown-item" onclick="location.href='/client/kredit'"><i style="position:absolute;top: 50%;transform: translateY(-50%);" class="fas fa-money-bill"></i>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Dobít kredit</a>
    <a style="position:relative;" class="dropdown-item" onclick="location.href='/client/historie'"><i style="position:absolute;top: 50%;transform: translateY(-50%);" class="fas fa-history"></i>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Historie účtu</a>
    <a style="position:relative;" class="dropdown-item" onclick="location.href='/client/mysql'"><i style="position:absolute;top: 50%;transform: translateY(-50%);" class="fas fa-database"></i>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;MySQL Databáze</a>
    <a style="position:relative;" class="dropdown-item" onclick="location.href='/client/tickets'"><i style="position:absolute;top: 50%;transform: translateY(-50%);" class="fas fa-ticket-alt"></i>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Tickety <span class="badge badge-light">0</span></a>
    <div class="dropdown-divider"></div>
    <a style="position:relative;" class="dropdown-item" onclick="location.href='/client/logout'"><i style="position:absolute;top: 50%;transform: translateY(-50%);" class="fas fa-sign-out-alt"></i>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Odhlásit se </a>
  </div>
</div>
  
</nav>
<script>

$('#profileDD').on('show.bs.dropdown', function () {
  document.getElementsByClassName("arrowdown")[0].style = "-webkit-transform: rotate(0deg);";
});
$('#profileDD').on('hide.bs.dropdown', function () {
  document.getElementsByClassName("arrowdown")[0].style = "-webkit-transform: rotate(-90deg);";
});

</script>  



<script>
    function logout(){
        window.location='https://pearhost.cz/client/logout';
    }
</script> 

<script>
    function admin(){
        window.location='https://pearhost.cz/admin';
    }
</script> 

<body style="background-color:#070c14">


<style>


.vrade {display:inline-block;}

        a:link {
            text-decoration: none;
        }
        a:hover {
            text-decoration: none;
        }

nav {
  display: grid;
  gap: 1rem;
  grid-template-columns: repeat(4, minmax(0, 1fr));
  /* 
  if we did this instead of the template it would be a problem:
  grid-auto-flow: column;
  */
  text-align: center;
  padding: 2rem 1rem;
}


html {
    overflow: scroll;
    overflow-x: hidden;
}
::-webkit-scrollbar {
    width: 0;  /* Remove scrollbar space */
    background: transparent;  /* Optional: just make scrollbar invisible */
}
/* Optional: show position indicator in red */
::-webkit-scrollbar-thumb {
    background: #FF0000;
}


body {
  color: rgb(220,221,222);
}

h1 {
  color: rgb(220,221,222);
}

h2 {
  color: rgb(220,221,222);
}

h3 {
  font-weight: 9000;
  color: rgb(220,221,222);
  font-size: 24px;
}

h4 {
  color: rgb(220,221,222);
  font-size: 18px;
}
@media (max-width : 800px) {
    #mobile_changesidebar_button {top:20px !important;}
    #pc_changesidebar_button {top: 20px !important;}
}
</style>



<style>
  .sidebar a:hover{
    box-shadow: 7.5px 0px 5px -5px #068B1C inset;
  }
  @keyframes spin {
    from {
        transform:rotate(0deg);
    }
    to {
        transform:rotate(360deg);
    }
  }
  .sidebar a:hover i{
    animation-name: spin;
    animation-duration: 0.75s; 
  }
  .sidebar a{
    position: relative;
  }
  .sidebar a i{
    height:16px;
    top: calc(50% - 8px);
    position:absolute;
    color:#068B1C;
    transition-duration: 0.75s;
  }
  .sidebar .active:hover i {
    animation: none;
  }
  .sidebar a.active i {
    position: relative !important;
    color:white;
    transform: none;
  }
  .sidebar {
    scrollbar-width: none;
    height:auto;
    position:fixed;
    user-select: none;
    bottom: 0;
    top:66px;
  }
</style>  


<div class="sidebar">
  
  <a class="active"><strong><i class="fas fa-caret-right"></i> MOJE SLUŽBY</strong></a>
    <a id="mcS" href="javascript:;" onclick="minecraft();"><i class="fas fa-cubes"></i>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Minecraft servery</a>
  <a id="vpsS" href="javascript:;" onclick="vps();"><i class="fas fa-server"></i>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;VPS servery</a>
  

  <a class="active"><strong><i class="fas fa-caret-right"></i> NOVÁ SLUŽBA</strong></a>
  <a  href="https://pearhost.cz/client/objednavka/?type=mc&id=2"><i class="fas fa-cubes"></i>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Objednat MC server</a>
  <a  href="https://pearhost.cz/client/objednavka/?type=vps&id=4"><i class="fas fa-server"></i>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Objednat VPS</a>
  
<a class="active" style="bottom:0;position:absolute;left:0;width:255px;text-align:center"><i class="fas fa-code-branch"></i> Administrace v0.5</a>
</div>

<div class="wrapper" style="padding:40px 16px;">

<div class="alert alert-warning alert-dismissible fade show" role="alert">Pozor! Administrace je v testovacím chodu, jsou možné výpadky konzole a podobné problémy.<button type="button" class="close" data-dismiss="alert" aria-label="Close">  <span aria-hidden="true">&times;</span></button></div>


<div class="card text-white bg-dark mb-3">
  <div class="">
  </div>

<div class="row">
  <div class="col-sm-6" style="flex:auto;max-width:none;">
    <div class="card text-white bg-dark mb-3 border-0">
      <div class="card-body">
      <h5 class="card-title"><i style="color:#068B1C;" class="fas fa-server"></i> Moje služby</h5>
  <p class="card-text">Níže naleznete seznam služeb, ke kterým máte přístup.</p>
      </div>
    </div>
  </div>
</div>
</div>




<section id="minecraft" style="display:active">
                                            
                                                

                <div class="mcrow" style="cursor:pointer;z-index:799"><div id="mc_84996.icon"><div class="mcicon" style="background-color:gray"><i style="font-size:175%;" class="fas fa-server"></i></div></div>
                <script>
                  function getMCStatemc_84996(){
                  $.get('https://pearhost.cz/api/getStateMC.php?id=mc_84996', function(data){
                    if(data == '1'){
                      document.getElementById('mc_84996.icon').innerHTML = '<div class="mcicon"><i style="font-size:175%;" class="fas fa-server"></i></div>';
                    }
                    if(data == '0'){
                      document.getElementById('mc_84996.icon').innerHTML = '<div class="mcicon" style="background-color:red"><i style="font-size:175%;" class="fas fa-server"></i></div>';
                    }
                  });
                  }
                  getMCStatemc_84996();

                  setInterval(function(){ 
                    if(document.visibilityState === 'visible'){
                      if(localStorage.getItem('selected') == 'mc'){
                        getMCStatemc_84996();
                      }
                    }
                  }, 1500);
                </script>
                <p class="mcname" style="float:left;">NuhnicekMc <span id="ipspan" style="color:darkgray;"> - 













cherry.pearhost.cz:40679 <span style="user-select: none" class="badge badge-info"><i class="fas fa-users"></i> <span data-playercounter-ip="













cherry.pearhost.cz:40679"><i class="fa fa-circle-o-notch fa-spin"></i> </span> hráčů</span> <span style="user-select: none" class="badge badge-primary"><i class="fas fa-stopwatch"></i> Expirace: 25.02.2022</span></span> 
                <div style="font-size:20px;position:absolute;right:30px;top:50%;transform: translateY(-50%);">
                <button class="btn btn-success dropdown-toggle" type="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                  <i class="fas fa-hammer"></i> Spravovat
                </button>
                <div class="dropdown-menu dropdown-menu-right">
                  <a onclick="startserver(`mc_84996`)" style="position:relative;" class="dropdown-item" href="javascript:;"><i class="fas fa-play" style="color:#28a745;position:absolute;top: 50%;transform: translateY(-50%);"></i>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Zapnout server</a>
                  <a onclick="stopserver(`mc_84996`)" style="position:relative;" class="dropdown-item" href="javascript:;"><i class="fas fa-pause" style="color:#ffc107;position:absolute;top: 50%;transform: translateY(-50%);"></i>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Vypnout server</a>
                  <a onclick="restartserver(`mc_84996`)" style="position:relative;" class="dropdown-item" href="javascript:;"><i class="fas fa-sync-alt" style="color:#007bff;position:absolute;top: 50%;transform: translateY(-50%);"></i>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Restartovat server</a>
                  <a onclick="killserver(`mc_84996`)" style="position:relative;" class="dropdown-item" href="javascript:;"><i class="fas fa-plug" style="color:#dc3545;position:absolute;top: 50%;transform: translateY(-50%);"></i>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Tvrdě vypnout server</a>
                  <div class="dropdown-divider"></div>
                  <a onclick="location.href=`/client/prodlouzeni/server/mc_84996`" style="position:relative;" class="dropdown-item" href="javascript:;"><i class="fas fa-coins" style="color:#FFD700;position:absolute;top: 50%;transform: translateY(-50%);"></i>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Prodloužit server</a>
                  <div class="dropdown-divider"></div>
                  <a onclick="location.href=`/client/konzole/server/mc_84996`" style="position:relative;" class="dropdown-item" href="javascript:;"><i class="fas fa-cogs" style="color:#17a2b8;position:absolute;top: 50%;transform: translateY(-50%);"></i>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Spravovat server</a>
                </div>
                </div>
                </p></div>

                                                
                                        


</section>



<section id="vps" style="display:none;">
<div class="row d-flex justify-content-start">
  <div class="vpsrow d-flex justify-content-center" style="height:auto;padding-bottom:15px;padding-top:15px;">
  <button onclick="zmenitVirtualizorHeslo();" type="button" stlyle="margin-right:10px;" class="btn btn-warning btn-lg"><i class="fas fa-key"></i> Změnit heslo od Virtualizoru</button>
  <button onclick="window.open('https://vps.pearhost.cz:4083', '_blank');" type="button" style="margin-left:10px;" class="btn btn-primary btn-lg">Přejít do Virtualizoru <i class="fas fa-arrow-right"></i></button>
  </div>
  </div>


</section>

<script>
function minecraft() {
  localStorage.setItem("selected", "mc");
  document.getElementById("minecraft").style = "display:active";
  document.getElementById("mcS").classList.add("knedlik");
  document.getElementById("vpsS").classList.remove("knedlik");
  document.getElementById("vps").style = "display:none";
}

function vps() {
  localStorage.setItem("selected", "vps");
  document.getElementById("minecraft").style = "display:none";
  document.getElementById("mcS").classList.remove("knedlik");
  document.getElementById("vpsS").classList.add("knedlik");
  document.getElementById("vps").style = "display:active";
}

minecraft();window.history.pushState({}, {}, '/client/');</script>

<script>
function zmenitVirtualizorHeslo(){
  const swalWithBootstrapButtons = Swal.mixin({
        customClass: {
        confirmButton: 'btn btn-success',
        cancelButton: 'btn btn-danger'
    },
        buttonsStyling: false
    });

    const email = swalWithBootstrapButtons.fire({
    icon: 'question',
    input: 'password',
    title: 'Změna Virtualizor hesla',
    showCancelButton: true,
    inputPlaceholder: 'Zadejte nové heslo',
    cancelButtonText: "Zrušit",
    }).then((result) => {
        if(result.isConfirmed){
            nevim("Zpracovávám požadavek...")
            var heslo = result.value
            $.get("https://pearhost.cz/client/api/changevirtualizorpasswd.php?heslo="+heslo, function(data){
              if(data.includes("hotovo")){
                uspesneM("Heslo bylo úspěšně změněno!")
              } else if(data.includes("chybiheslo")){
                neuspesneM("Vyplňte prosím heslo!")
              } else if(data.includes("spatnyucet")){
                neuspesneM("Pro tento email není přiřazený žádný Virtualizor účet.")
              } else {
                neuspesneM("Nastala neočekávaná chyba. Kontaktujte podporu.")
              }
            })
        }
    })
}


function notOffline(element) {
    Swal.fire({
      title: 'Před reinstalací prosím vypněte Váš server.',
      toast: true,
      showConfirmButton: false,
      position: 'top-end',
      icon: 'error',
      timer: 4000,
      timerProgressBar: true,
})
}

function serverReinstall(element) {
    Swal.fire({
      title: 'Server byl úspěšně reinstalován!',
      toast: true,
      showConfirmButton: false,
      position: 'top-end',
      icon: 'success',
      timer: 6000,
      timerProgressBar: true,
})
}


function kredity(element) {
    Swal.fire({
      title: 'Na Vašem účtě se nachází 10 kreditů.',
      toast: true,
      showConfirmButton: false,
      position: 'top-end',
      icon: 'info',
      timer: 2000,
      timerProgressBar: true,
})
}
</script>

<script>
function uspesneM(text){
  Swal.fire({
      title: text,
      toast: true,
      showConfirmButton: false,
      position: 'top-end',
      icon: 'success',
      timer: 4000,
      timerProgressBar: true,
})
}
function neuspesneM(text){
  Swal.fire({
      title: text,
      toast: true,
      showConfirmButton: false,
      position: 'top-end',
      icon: 'error',
      timer: 4000,
      timerProgressBar: true,
})
}
function nevim(text){
  Swal.fire({
      title: text,
      toast: true,
      showConfirmButton: false,
      position: 'top-end',
      icon: 'question',
      timer: 5000,
      timerProgressBar: false,
})
}


function uspesne(element) {
  Swal.fire({
      title: 'Byl jsi úspěšně přihlášen!',
      toast: true,
      showConfirmButton: false,
      position: 'top-end',
      icon: 'success',
      timer: 4000,
      timerProgressBar: true,
})
}
</script>

<script>
function errorauth(element) {
  Swal.fire({
      title: 'Přístup byl zamítnut, jedná se o chybu? Kontaktujte nás!',
      toast: true,
      showConfirmButton: false,
      position: 'top-end',
      icon: 'error',
      timer: 5000,
      timerProgressBar: true,
})
}
</script>

<script>
function odeslan(element) {
  Swal.fire({
      title: 'Příkaz byl úspěšně odeslán!',
      toast: true,
      showConfirmButton: false,
      position: 'top-end',
      icon: 'success',
      timer: 4000,
      timerProgressBar: true,
})
}
</script>


</html>




<script>
function restartserver(server) {
  $.get("https://pearhost.cz/api/restartapi.php?id="+server, function(data){
    if(data.includes("hotovo")){
      uspesneM("Požadavek na restart serveru byl úspěšně odeslán!");
    } else if(data.includes("limit")){
      neuspesneM("Počkejte prosím před odesíláním další akce!");
    } else {
      neuspesneM("Nastala chyba systému!");
    }
  });
}
</script>

<script>
function startserver(server) {
  $.get("https://pearhost.cz/api/startapi.php?id="+server, function(data){
    if(data.includes("hotovo")){
      uspesneM("Požadavek na start serveru byl úspěšně odeslán!");
    } else if(data.includes("limit")){
      neuspesneM("Počkejte prosím před odesíláním další akce!");
    } else {
      neuspesneM("Nastala chyba systému!");
    }
  });
}
</script>

<script>
function stopserver(server) {
  $.get("https://pearhost.cz/api/stopapi.php?id="+server, function(data){
    if(data.includes("hotovo")){
      uspesneM("Požadavek na stop serveru byl úspěšně odeslán!");
    } else if(data.includes("limit")){
      neuspesneM("Počkejte prosím před odesíláním další akce!");
    } else {
      neuspesneM("Nastala chyba systému!");
    }
  });
}
</script>

<script>
function killserver(server) {
  $.get("https://pearhost.cz/api/killapi.php?id="+server, function(data){
    if(data.includes("hotovo")){
      uspesneM("Požadavek na tvrdé vypnutí serveru byl úspěšně odeslán!");
    } else if(data.includes("limit")){
      neuspesneM("Počkejte prosím před odesíláním další akce!");
    } else {
      neuspesneM("Nastala chyba systému!");
    }
  });
}
</script>













</body>
