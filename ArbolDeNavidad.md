# Compiladores - Árbol De Navidad
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ÁRBOL DE NAVIDAD</title>
<style>
body{ background: black; display: grid; justify-content: center; text-align: center; }
h1{ color: greenyellow;}
p{ color: teal; }
.estrella{font-size: 100px; animation: colores 1s infinite;}
.rojo{
color:red;
transition: all 1.5s;
Cristofer Galarza, Esteban Bajaña, Ariel Suntasig
font-size: 30px;
}
@keyframes colores {
0%{ color: red;}
33%{ color: white;}
66%{ color: blue;}
100%{ color: orange;}
}
</style>
</head>
<body>
<div class="estrella">*</div>
<div id="arbol"></div>
<h1>FELIZ NAVIDAD!! Y PRÓSPERO AÑO NUEVO 2022</h1>
<script>
var hojas = "";
[10,2].forEach(row => {
new Array(row).fill('').forEach((v,i) => {
hojas += ([
...Array(9-i).fill("<span> </span>"),
...Array(1+i*2).fill("<span class='rojo'>*</span>"),
...Array(9-i).fill("<span> </span>"),
].join(''))
hojas += "<br>"
})
})
document.getElementById("arbol").innerHTML = hojas;
let animacion = document.querySelectorAll(".rojo");
animacion.innerHTML = hojas;
function animar(){
for( var i =0 ; i<animacion.length; i++){
let tiempo = i/20 +1
animacion[i].style.animation = "colores "+tiempo+"s infinite"
}
}
window.addEventListener('load',animar)
</script>
</body>
</html>
