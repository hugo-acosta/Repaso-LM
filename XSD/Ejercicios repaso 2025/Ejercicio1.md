``` xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE aeropuerto [
  <!ELEMENT aeropuerto (avion+, puertas_embarque)>
    <!ELEMENT avion (modelo, compania, capacidad, crew, pasajeros)>
      <!ELEMENT modelo (#PCDATA)>  
      <!ELEMENT compania (#PCDATA)>  
      <!ELEMENT capacidad (#PCDATA)>  
      <!ELEMENT crew (piloto, copiloto, flight_attendance+)>  
      <!ELEMENT pasajeros (pasajero+)>
        <!ELEMENT piloto (#PCDATA)>  
        <!ELEMENT copiloto (#PCDATA)>  
        <!ELEMENT flight_attendance (nombre)>  
          <!ELEMENT nombre (#PCDATA)>  
        <!ELEMENT pasajero (nombre, nacionalidad, maletas)>  
          <!ELEMENT nacionalidad (#PCDATA)>
          <!ELEMENT maletas (maleta+)>
            <!ELEMENT maleta (#PCDATA)>
            <!ATTLIST maleta peso CDATA #REQUIRED>
        <!ATTLIST pasajero id ID #REQUIRED>
    <!ATTLIST avion id ID #REQUIRED>
  
    <!ELEMENT puertas_embarque (puerta+)>
      <!ELEMENT puerta (#PCDATA)>
      <!ATTLIST puerta id ID #REQUIRED>
]>
```