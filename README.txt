var sexo=[];
var edad=[];
var hora=[];
var sexH=[];
var numHombres="";
var edadMax="";
var mediaHora="";

function maxEdad(edad1,max){
  for (let i = 0; i < edad1.length; i++) {
    for (let j = 0; j < edad1.length; j++) {
      if (edad1>max) {
        max=edad1[i];
      }
    }
}
console.log(`La edad maxima es ${max}`);
}

function medHoras(hora1,med){
  for (let i = 0; i < hora1.length; i++) {
      med=hora1[i]+med;
      }
      med=med/hora1.length;
      console.log(`La media de horas es ${med}`);
    }


while (true) {
  var respSexo=prompt("Escribe tu sexo: M o H");
  if (respSexo=="H" || respSexo=="M") {
    sexo.push(respSexo);
  }
  else {
    if (respSexo=="Salir") {
    maxEdad(edad,edadMax);
    medHoras(hora,mediaHora);
    break;
    }
    var respSexo="";
    while ((respSexo!="H") && (respSexo!="M")) {
      respSexo=prompt("Escribe tu sexo: M o H");
    }
    sexo.push(respSexo);
  }

  var respEdad=Number(prompt("Escribe edad"));
  if (respEdad>="18") {
    edad.push(respEdad);
  }
  else {
    if (respEdad=="Salir") {
      numeroHombres(sexo,numHombres);
      maxEdad(edad,edadMax);
      medHoras(hora,mediaHora);
      break;
    }
    while (respEdad<"18") {
      respEdad=Number(prompt("Escribe edad"));
  }
  edad.push(respEdad);
}
  var respHora=prompt("Escribe el numero de horas que juegas a la consola al dia");
  if (respHora>"0") {
    hora.push(respHora);
  }
  else {
    if (respHora=="Salir") {
      numeroHombres(sexo,numHombres);
      maxEdad(edad,edadMax);
      medHoras(hora,mediaHora);
      break
    }
    while (respHora<="0") {
      respHora=prompt("Escribe el numero de horas que juegas a la consola al dia");
  }
  hora.push(respHora);
}
}
