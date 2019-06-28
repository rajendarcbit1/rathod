<?php
session_start();
?>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
* {
  box-sizing: border-box;
}

/* Create three unequal columns that floats next to each other */
.column {
  float: left;
  padding: 10px;
  height: 600px; /* Should be removed. Only for demonstration */
}

.left {
  width: 20%;
  height:85%;
}

.right {
  width: 60%;
  height:85%;
}
.ri{
  width: 20%;
  height:85%;
}

/* Clear floats after the columns */
.row:after {
  content: "";
  display: table;
  clear: both;
}
 h3{color:green;}
 h2{color:red;}
 .home{
  width: 100%;
  height:6%;}
  p.A{position:absolute;
		left:470px;top:150px;}
 p.N{
        position:absolute;
		left:400px;top:200px;}
 p.K{
        position:absolute;
		left:510px;top:210px;}
p.ME{
        position:absolute;
		left:410px;top:260px;}
p.WA{
        position:absolute;
		left:550px;top:270px;}
p.KH{
        position:absolute;
		left:700px;top:285px;}
p.RA{
        position:absolute;
		left:380px;top:313px;}
p.NA{
        position:absolute;
		left:520px;top:350px;}
p.MA{
        position:absolute;
		left:370px;top:400px
		}
 .x{
        position:absolute;
		left:770px;top:120px;
		color:green;}
    p.A1{position:absolute;
		left:120px;top:150px;}
	p.A2{position:absolute;
		left:120px;top:200px;}
    p.A3{position:absolute;
		left:120px;top:250px;}
    p.A4{position:absolute;
		left:120px;top:300px;}
	p.A5{position:absolute;
		left:120px;top:350px;}
</style>
</head>
<body>
<h1 align="center"><font color="green">AGRICULTURE MANAGEMENT SYSTEM <br/> </font></h1>
<link rel="stylesheet" type="text/css" href="nav.css">
<div id="main">
<div class="row">
<nav role="navigation">	
  <div class="row home" style="background-color:green;">
	<div style="float:right; font-size:20px;margin-top:15px;">
			<?php
			 if(isset($_SESSION['name']))	
			 {
			 echo "Welcome,".$_SESSION['name']."&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href=\"logout.php\" class=\"btn btn-info\">Logout</a>";
			 }
			 else
			 {
			 ?>
				<a href="login.php" class="btn btn-info">Login</a>&nbsp;&nbsp;&nbsp;&nbsp;
			<?php } ?>
</nav>
</div>


<div class="row">
  <div class="column left" style="background-color:#aaa;">
    <h3>MAJOR CROPS</h3>
	<ol>
	 <p class="A1"><a href="rice.php" target="_top">1.RICE</a></p>
     <p class="A2"><a href="wheat.php" target="_top">2.WHEAT</a></p>
	 <p class="A3"><a href="maize.php" target="_top">3.MAIZE</a></p>
	 <p class="A4"><a href="sugarcan.php" target="_top">4.SUGARCAN</a></p>
	 <p class="A5"><a href="puleses.php" target="_top">5.PULESES</a></p>
   </ol>
   </div>
  <div class="column right" style="background-color:#ccc;">
   <img src="ts04.png"></img>
</div>
	<div class="column ri" style="background-color:#aaa;">
    <h2>ADMIN DETIALS </h2>
	<li><a href="admin.php" target="_top">ADMIN LOGIN</a></li><li>
</div>
/* link the district links */
<p class="A"><a href="adilabad.php" target="_top">ADILABAD</a></p>
<p class="N"><a href="nizambad.php" target="_top">NIZAMABAD</a></p>
<p class="K"><a href="karimnagar.php" target="_top">KARIMNAGAR</a></p>
<p class="ME"><a href="medak.php" target="_top">MEDAK</a></p>
<p class="WA"><a href="warangal.php" target="_top">WARANGAL</a></p>
<p class="KH"><a href="khamman.php" target="_top">KHAMMAN</a></p>
<p class="RA"><a href="rangareddy.php" target="_top">RANGAREDDY</a></p>
<p class="NA"><a href="nalgonda.php" target="_top">NALGONDA</a></p>
<p class="MA"><a href="mahabu.php" target="_top">MAHBUBNAGAR</a></p>
<p class="x"><a href="graph.php" target="_top">TELENGANA</a></p>
</body>
</html>
<?php

if(isset($_SESSION['error']))
{
session_destroy();
}

?>
