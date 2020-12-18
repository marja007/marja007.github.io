# marja007.github.io

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">

<title>Tentti</title>
</head>
<body>
    <h1>Tehtävä 1</h1>
    <form>
        <label>Panos:</label> 
            <input type="text" id="panos" size="3"> <br><br>
        <input type="button" value="Pelaa" onclick="pelaa()">
      </form>
      <div id="vastaus"></div>
<script>
function pelaa(){
var panos=document.getElementById("panos").value;
var noppa1=Math.round((Math.random()*5)+1);
var noppa2=Math.round((Math.random()*5)+1);
var noppa3=Math.round((Math.random()*5)+1);
var lasku=panos*50;
var lasku1=panos*5;
var lasku3=panos*2;
var voitto;
if(noppa1 <6 && noppa2<6 && noppa3<6){
voitto=0
}else if(noppa1==6|| noppa2==6 || noppa3==6){
    voitto=lasku3
}else if(noppa1==6 && noppa2==6 && noppa3==6){
    voitto=lasku
}else{voitto=lasku1
}
document.getElementById("vastaus").innerHTML="<p>Nopat olivat "+ noppa1+" "+noppa2+" "+noppa3+
    "<br>Voitto oli "+voitto.toFixed(2)+ " euroa"
}
</script>
</head>
<body>
    <h1>Tehtävä 2</h1>
    <form>
        <label>Hinta:</label> 
            <input type="text" id="hinta" size="8"> <br><br>
        <label>Määrä:</label> 
            <input type="text" id="maara" size="8"> <br><br>
        <input type="button" value="Laske" onclick="laske()">
      </form>
      <div id="vastaus2"></div>
<script>
function laske(){
    var hinta=parseInt(document.getElementById("hinta").innerHTML.value);
    var maara=parseInt(document.getElementById("maara").innerHTML.value);

    var jouluale=joulu();
    var maaraale=alennus(maara);
    var lopputulos=hinta-jouluale-maaraale
document.getElementById("vastaus2").innerHTML= "Yksi lippu maksaa " + lopputulos;
}

function joulu(){
    var paiva =new Date
    var kuukausi=paiva.getMonth
    var hinta1
    if(kuukausi==12){
        hinta1=(hinta*0.2)/maara
    }
    return joulu
}
function alennus(maara){
    if (maara>=10){
        var hinta2=(hinta*0.1)/maara
    }
    return alennus
}

</script>

    <h1>Tehtävä 3</h1>
    <form>
        <label>a tehtävä</label> 
           
            <input type="button" value="Listaa kaikki" onclick="listaa()">
      </form>
      <div id="vastaus3"></div><p></p>
<script>
var toiveet = [ 
{nimi: "Pekka",toive:"Kinky Boots"}, 
{nimi: "Matti",toive:"PlayStation 5 (PS5) pelikonsoli"},
{nimi: "Pekka",toive:"Tehosekoitin Wilfa"},
{nimi: "Liisa",toive:"Nyrkkeilysäkki"},
{nimi: "Matti",toive:"Marvel s Spider-Man: Miles Morales (PS5)"},
{nimi: "Liisa", toive:"Yöasu", hinta: 49.90},
{nimi: "Matti", toive:"Sackboy: A Big Adventure (PS5)", hinta: 64.90},
{nimi: "Pekka", toive:"Kirja Hyvän historia", hinta: 21.95},
{nimi: "Pekka", toive:"Rubikin kuutio", hinta: 7.95},
{nimi: "Matti",toive:"Suklaarasia", hinta: 3.90},
];
function listaa(){
    var teksti="";
    for (var i=0; i<toiveet.length;i++){
        teksti=teksti+toiveet[i].nimi+": "+toiveet[i].toive+"<br>";
    }
    document.getElementById("vastaus3").innerHTML=teksti;
}

</script>
<form>
    <label>b tehtävä</label> 
    <label>Nimi:</label> 
    <input type="text" id="etsittava" size="8"> <br><br>
        <input type="button" value="Hae toiveet" onclick="etsi()">
  </form>
  <div id="vastaus4"></div><p></p>
<script>
var toiveet = [ 
{nimi: "Pekka",toive:"Kinky Boots",hinta:69}, 
{nimi: "Matti",toive:"PlayStation 5 (PS5) pelikonsoli", hinta:529},
{nimi: "Pekka",toive:"Tehosekoitin Wilfa", hinta:65},
{nimi: "Liisa",toive:"Nyrkkeilysäkki", hinta:65.30},
{nimi: "Matti",toive:"Marvel s Spider-Man: Miles Morales (PS5)", hinta:59.95},
{nimi: "Liisa", toive:"Yöasu", hinta: 49.90},
{nimi: "Matti", toive:"Sackboy: A Big Adventure (PS5)", hinta: 64.90},
{nimi: "Pekka", toive:"Kirja Hyvän historia", hinta: 21.95},
{nimi: "Pekka", toive:"Rubikin kuutio", hinta: 7.95},
{nimi: "Matti",toive:"Suklaarasia", hinta: 3.90},
];
function etsi(){
    var etsittava=document.getElementById("etsittava").value;
    var tekst="";
    for (var i=0; i<toiveet.lenght;i++){
        if(toiveet.nimi[i]==etsittava){
            tekst=tekst+toiveet[i].toive+"<br>";
        }else{
            tekst="Yhtään lahjatoivetta ei ollut "+etsittava
        }
       
    }
    document.getElementById("vastaus4").innerHTML=etsittava+"n lahjatoiveet olivat:<br>"+tekst;
}
</script>
<form>
    <label>c tehtävä</label> 
    <label>Nimi:</label> 
    <input type="text" id="lisanimi" size="8"> <br><br>
    <label>Toive:</label> 
    <input type="text" id="lisatoive" size="8"> <br><br>
    <label>Hinta:</label> 
    <input type="text" id="lisahinta" size="8"> <br><br>
        <input type="button" value="Lisää" onclick="lisaa()">
  </form>
  <div id="vastaus4"></div><p></p>
<script>
var toiveet = [ 
{nimi: "Pekka",toive:"Kinky Boots",hinta:69}, 
{nimi: "Matti",toive:"PlayStation 5 (PS5) pelikonsoli", hinta:529},
{nimi: "Pekka",toive:"Tehosekoitin Wilfa", hinta:65},
{nimi: "Liisa",toive:"Nyrkkeilysäkki", hinta:65.30},
{nimi: "Matti",toive:"Marvel s Spider-Man: Miles Morales (PS5)", hinta:59.95},
{nimi: "Liisa", toive:"Yöasu", hinta: 49.90},
{nimi: "Matti", toive:"Sackboy: A Big Adventure (PS5)", hinta: 64.90},
{nimi: "Pekka", toive:"Kirja Hyvän historia", hinta: 21.95},
{nimi: "Pekka", toive:"Rubikin kuutio", hinta: 7.95},
{nimi: "Matti",toive:"Suklaarasia", hinta: 3.90},
];
function lisaa(){
var lisattavanimi=document.getElementById("lisanimi").value;
var lisatoive=document.getElementById("lisatoive").value;
var lisahinta=document.getElementById("lisahinta").value;
var paikka=toiveet.length;
toiveet[paikka]=lisattavanimi+lisatoive+lisahinta;

}

</script>
</body>
</html>

