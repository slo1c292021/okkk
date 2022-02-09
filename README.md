<!DOCTYPE HTML>
<html lang="pl">
<head>
	<meta charset="utf-8" />
	<title>Odliczanie dni do wydarzenia </title>
	
	<script type="text/javascript" >

	
	function odliczanie()
	{
		var dzisiaj = new Date();//obiekat Date 
		
		var dzien = dzisiaj.getDate();
		var miesiac = dzisiaj.getMonth()+1;
		var rok = dzisiaj.getFullYear();
		var milisekundy = dzisiaj.getTime();
		
		var end = new Date("06/25/2021");//data wydarzenia
		var endDzien = end.getDate();
		var endMiesiac = end.getMonth()+1;
		var endRok = end.getFullYear();
		var milisekundy2 = end.getTime();
		
		var pozostalo = milisekundy2 - milisekundy; //obliczamy ile milisekund pozostało do wydarzenia
		var dni = Math.floor(pozostalo/86400000); //obliczamy liczbe dni do wydarzenia
		
	
		
		document.getElementById("aktualnaData").innerHTML = "Aktualna data: "+dzien+"/"+miesiac+"/"+rok; 
		document.getElementById("dataWydarzenia").innerHTML = "Data wydarzenia do którego obliczamy liczbę dni: "+endDzien+"/"+endMiesiac+"/"+endRok;
		document.getElementById("dniDoWydarzenia").innerHTML ="Do wydarzenia pozostało: "+ dni;
		 
	}
	
	</script>

	<link rel="stylesheet" href="cssnew 1.txt" type="text/css" />
	
</head>
<body>

<div id="container">
<div id="topBar">
	
	<div id="aktualnaData">...</div> 

	<br/>
	
	<div id="dataWydarzenia">...</div>
<br/>
<br/>	
	
	<div id="dniDoWydarzenia">...</div> 
	
	<script type="text/javascript" >
	odliczanie();
</script>
<div id="footer">
</div>
</div>
</body>
</html>
