# assignment-

<!DOCTYPE html>
<html>
<head>
​<link href="https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css" rel="stylesheet">
​<link rel="preconnect" href="https://fonts.gstatic.com">
<link href="https://fonts.googleapis.com/css2?family=Poppins&display=swap" rel="stylesheet">
 
​<title></title>
</head>
<body>
<div class="container">
<div class="card">​
​<h2><i class="fa fa-map-marker"></i><span id="location"></span></h2>
​<h6 id="weather"></h6>
​<h4><span id="temp"></span></h4>
​<img src="" id="icon">
​<button onclick="window.location.reload();" class="refresh"><i class="fa  fa-refresh"></i></button>
</div>
</div>
<script type="text/javascript">
​link="https://api.openweathermap.org/data/2.5/weather?q=hyderabad&units=metric&appid=9aa51f25956d8a7c5b6a05773c9dfafb";
​var request = new XMLHttpRequest();
​request.open('GET', link,true);
​request.onload = function(){
​​var obj =JSON.parse(this.response);
​​console.log(obj);
​​
​​document.getElementById('weather').innerHTML=obj.weather[0].description;
​​document.getElementById('location').innerHTML=obj.name;
​​document.getElementById('temp').innerHTML=obj.main.temp+"°f";
​​document.getElementById('icon').src="http://openweathermap.org/img​/w/"+obj.weather[0].icon+".png";
 
​​
​}
​if(request.status==200){
​​console.log("error");
​}
​request.send();
</script>
<script src="https://apps.elfsight.com/p/platform.js" defer></script>
<div class="elfsight-app-66bedf22-28c9-4629-90bc-a19e488c56dc"></div>
</body>
</html>
 
