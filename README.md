<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
body {
  margin: 0;
  font-family: Arial, Helvetica, sans-serif;
}

.topnav {
  overflow: hidden;
  background-color: #f2f2f2;
}

.topnav a {
  float: left;
  color: #b1b1b1;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
  font-size: 17px;
}

.topnav a:hover {
  background-color:#b1b1b1; 
  color: black;
}

.topnav a.active {
  background-color: #d1b8e0; /* Violetti tausta auki olevaan sivuun */
  color: white;
}

footer {
  position: fixed;
  left: 0;
  bottom: 0;
  width: 100%;
  background-color: #d1b8e0; /* Vaalean violetti tausta */
  color: white;
  text-align: center;
  padding: 20px;
  font-size: 12px; /* Pienempi fontti alareunassa */
}

img {
  width: 100%;
  height: auto;
  display: block;
}

.content {
  display: none; /* Piilota sisältö aluksi */
  padding-left: 25px;
}

.show { display: block; } /* Näytä sisältö klikatun sivun mukaan */

</style>
</head>
<body>

<div class="topnav">
  <a href="#" onclick="showPage('ETUSIVU')">ETUSIVU</a>
  <a href="#" onclick="showPage('KUKAOLEN')">KUKA OLEN</a>
  <a href="#" onclick="showPage('CV')" class="active">CV</a> <!-- CV on nyt kolmas sivu ja auki oleva -->
</div>

<div class="content" id="ETUSIVU">
  <h2>Etusivu</h2>
  <p>Tämä on etusivun sisältöä.</p>
</div>

<div class="content" id="KUKAOLEN">
  <h2>Kuka Olen</h2>
  <p>Tämä on "Kuka Olen" -sivun sisältöä.</p>
</div>

<div class="content" id="CV">
  <h2></h2>
  <p>
    <img src="CVH.png" alt="CV">
  </p>
</div>

<footer>
  <p>Yhteystiedot: Henniina.97@hotmail.com</p> 
</footer>

<script>
function showPage(pageName) {
  var i, tabcontent, tablinks;
  tabcontent = document.getElementsByClassName("content");
  for (i = 0; i < tabcontent.length; i++) {
    tabcontent[i].style.display = "none"; // Piilota kaikki sivut
  }
  document.getElementById(pageName).style.display = "block"; // Näytä valittu sivu
}
</script>

</body>
</html>
