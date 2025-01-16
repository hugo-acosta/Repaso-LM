``` xml
<aeropuerto>
    <avion id="A320">
        <modelo>Airbus A320</modelo>
        <compania>Iberia</compania>
        <capacidad>180</capacidad>
        <crew>
            <piloto>Antonio López</piloto>
            <copiloto>María Sánchez</copiloto>
            <flight_attendance>
                <nombre>Laura García</nombre>
            </flight_attendance>
            <flight_attendance>
                <nombre>Pedro Martínez</nombre>
            </flight_attendance>
        </crew>
        <pasajeros>
            <pasajero id="P001">
                <nombre>Juan Pérez</nombre>
                <nacionalidad>Española</nacionalidad>
                <maletas>
                    <maleta peso="12.5">Roja</maleta>
                    <maleta peso="8.0">Negra</maleta>
                </maletas>
            </pasajero>
            <pasajero id="P002">
                <nombre>Laura Gómez</nombre>
                <nacionalidad>Mexicana</nacionalidad>
                <maletas>
                    <maleta peso="15.0">Azul</maleta>
                </maletas>
            </pasajero>
        </pasajeros>
    </avion>
    <avion id="B737">
        <modelo>Boeing 737</modelo>
        <compania>Ryanair</compania>
        <capacidad>189</capacidad>
        <crew>
            <piloto>Carlos Ruiz</piloto>
            <copiloto>Sofía Fernández</copiloto>
            <flight_attendance>
                <nombre>Elena Torres</nombre>
            </flight_attendance>
            <flight_attendance>
                <nombre>Javier Gómez</nombre>
            </flight_attendance>
        </crew>
        <pasajeros>
            <pasajero id="P003">
                <nombre>Emily Johnson</nombre>
                <nacionalidad>Estadounidense</nacionalidad>
                <maletas>
                    <maleta peso="10.0">Negra</maleta>
                    <maleta peso="5.0">Verde</maleta>
                </maletas>
            </pasajero>
            <pasajero id="P004">
                <nombre>Michael Brown</nombre>
                <nacionalidad>Canadiense</nacionalidad>
                <maletas>
                    <maleta peso="20.0">Gris</maleta>
                </maletas>
            </pasajero>
            <pasajero id="P005">
                <nombre>Ana Martínez</nombre>
                <nacionalidad>Española</nacionalidad>
                <maletas>
                    <maleta peso="7.0">Rosa</maleta>
                    <maleta peso="12.0">Negra</maleta>
                </maletas>
            </pasajero>
        </pasajeros>
    </avion>
    <avion id="B777">
        <modelo>Boeing 777</modelo>
        <compania>Delta Airlines</compania>
        <capacidad>207</capacidad>
        <crew>
            <piloto>Juan Ramírez</piloto>
            <copiloto>Ángel Díaz</copiloto>
            <flight_attendance>
            <nombre>Javier Ibarra</nombre>
            </flight_attendance>
            <flight_attendance>
                <nombre>Juan Miguel González</nombre>
            </flight_attendance>
            <flight_attendance>
                <nombre>Leonor García</nombre>
            </flight_attendance>
        </crew>
        <pasajeros>
            <pasajero id="P006">
                <nombre>José Jiménez</nombre>
                <nacionalidad>Española</nacionalidad>
                <maletas>
                    <maleta peso="6.5">Azul</maleta>
                </maletas>
            </pasajero>
            <pasajero id="P007">
                <nombre>Will Smith</nombre>
                <nacionalidad>Estadounidense</nacionalidad>
                <maletas>
                    <maleta peso="9.25">Roja</maleta>
                    <maleta peso="12.5">Verde</maleta>
                </maletas>
            </pasajero>
            <pasajero id="P008">
                <nombre>François Serrats</nombre>
                <nacionalidad>Francesa</nacionalidad>
                <maletas>
                    <maleta peso="8.0">Blanca</maleta>
                    <maleta peso="5.0">Marrón</maleta>
                </maletas>
            </pasajero>
        </pasajeros>
        
    </avion>
    <puertas_embarque>
        <puerta id="A1">Abierta</puerta>
        <puerta id="B2">Cerrada</puerta>
        <puerta id="C3">Abierta</puerta>
        <puerta id="D4">Abierta</puerta>
    </puertas_embarque>
</aeropuerto>
```